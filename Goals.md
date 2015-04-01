#Goals

Defining the reason for going agile and what you hope to accomplish is a very important first step in going agile. Linking goals to overall business goals will help keep the team aligned and focused on the same end results.

Having the entire business invested in agile is very important to actually going agile. Moving an enterprise waterfall team to agile is virtually impossible, in my opinion, without agreement from the individual teams up to top level executives. Taking some time to define an initial set of goals will help give a common target to focus on while you begin your going agile journey.

##Perspective

These goals are overwhelmingly slanted towards my automation team and achieving continuous delivery. Automation and continuous delivery goals from our executives was the primary accelerant in our going agile story. The perspective gained from formulating goals based on core business goals gave us a clear target to shoot for.

To give you some perspective on the reason for our team going agile, below I present the goals I laid out for my small team. These goals are linked to the overall team and corporate goals. In addition to goals, I included some important principles and practices to help achieve each goal. 

These goals have evolved as we came to better understand where we wanted to go with agile and they continue to change to day as our perspective changes and situations change.

##My Team Goals

###Increase the amount of value delivered to end users

- Increase the quality of the product we deliver to end users
  - Improve automated testing
    - Create maintainable tests
      - Use Page Objects
      - Reduce duplication
      - Care for test code like production code
  - Reduce feedback loops
    - Keep tests fast
  - Test in environments that are as close to production as possible
    - Infrastructure as code
    - Validate new server nodes and network before use
  - Measure the amount of value to end users
  - Monitor value measures to determine success and failure

###Increase the flow of value to end users

- Identify, protect, and improve bottlenecks
  - Map value stream
- Decouple the architecture so that delivery (build, deploy, test, rollback...) can happen at component level
- Make delivery easy... push button
- Reduce feedback loops
    - Keep delivery pipeline fast
    - Provide continuous feedback for each step of the delivery process 
- Measure the flow of value to customers
- Monitor flow measurements to determine success and failure

###Improve the work experience

- Blameless culture
- Self organized teams
- Improve communication
- Make feedback openly visible
- Conduct postmortems and poll team to determine success and failure