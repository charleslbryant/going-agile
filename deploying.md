#Deploying

##Application Deployment

##Database Deployment

###Before Agile

The database deployment automation task scripts are written in NAnt. The deployment server runs the NAnt file and calls a target to orchestrate the deployment process. This is a high level overview of the work flow:

####Workflow

- Configure master database connection string.
- Create objects for each database included in a text file that has each database on a new line.
    - Configure database connection string. 
    - Drop database objects
        - SP - stored procedures
        - V - views
        - FN - scalar functions
        - TF - table functions
        - IF - in-lined table-functions
        - TR - SQL DML triggers
        - Service Broker Objects
            - sys.services where service_id > 100
            - sys.service_contracts where service_contract_id > 100
            - sys.service_message_types where message_type_id > 100
            - sys.service_queues where name not in ('ServiceBrokerQueue','QueryNotificationErrorsQueue','EventNotificationErrorsQueue')
    - If the database is a special type of event database
        - Deploy event objects
            - Triggers
            - UDFs
            - Views
            - Stored Procedures
            - Service Broker Objects
                - Message Types
                - Contracts
                - Queues
                - Services 
                - Routes
    - Deploy objects
        - Triggers
        - UDFs
        - Views
        - Stored Procedures
        - Service Broker Objects
                - Message Types
                - Contracts
                - Queues
                - Services 
                - Routes

#### Process

This work flow works by running SQL files from a source repository to drop and recreate database objects. When a developer makes a change to a database object they make the change in an SQL file and commit the change to the source repository. When the deployment runs the server downloads updates from the source repository. Then the deployment goes through the work flow above and runs the updated SQL files on the databases. 

####Issues

The problem with this deployment strategy is schema changes are never deployed. If an object change requires a corresponding schema change it may blow up the deployment. For example, we need to query a new table column. The column changed in a stored procedure and corresponding table script. The process doesn't run the table scripts so the column isn't created. When the new stored procedure runs it will fail because the column doesn't exits on the table. 

As illustrated above, developers do store schema changes in the source repository. The changes are create scripts, not alters, so you can't run them on existing tables. To update the schema you have to drop the table and run the create script. This is not a viable solution for deploying to production or environments that you care about data loss in.

When there are no schema changes involved this deployment strategy is easy to rollback. You just deploy an earlier commit from the source repository. Again, if there were any schema changes you will be in a world of hurt trying to rollback.

We do make schema changes in our regression tests. The test script drops and recreates the tables with the create scripts from the source repository. This works in this instance because we want to have fresh data in each regression test run to cut down on flaky tests.

###After Agile

Once we decided to go agile with our deployment process we needed to solve the schema update issue. Our DBA decided to write scripts that would automate the process by leveraging a paid tool from Red Gate called SQL Compare.
