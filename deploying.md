# Deploying

##Database Deployment

###Before Agile

The database deployment automation task scripts are written in NAnt. The deployment server runs the NAnt file and calls a target to orchestrate the deployment process. This is a high level overview of the workflow:

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

This work flow works by running sql files that are kept in the source repository. When a developer needs to make a change to a database object they make the change to the sql file and commit the change to the source repository. When the deployment is triggered the  server will download updates from the source repository and the work flow above runs the updated sql files on the databases. 

####Issues

The problem with this deployment strategy is schema changes are never deployed. If an object was updated that requires a corresponding schema change it may blow up the deployment. Developers do store schema changes in the database, but they are stored in create scripts, not alters. So, to update schema you have to first drop the table being changed, including its indexes, relations... etc., and run the create script. This is obviously not a viable solution for deploying to production or environments that you care about data loss in.

This deployment strategy is easy to rollback, when there are no schema changes involved. Just deploy an earlier commit from the source repository and the database objects will be created from that commit. Again, if there were any schema changes you will be in a world of hurt trying to rollback.

One side note, we had a process in our regression test script that would drop and recreate all of the tables with the scripts from the source repository. This works in this instance because we want to have fresh data in each regression test run to cut down on flaky tests.

###After Agile

Once we decided to go agile with our deployment process we needed to solve the schema update issue. Our DBA decided to write scripts that would automate the process by leveraging a paid tool from Red Gate called SQL Compare.
