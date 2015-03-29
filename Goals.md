#Goals

To give some perspective on the reason for our team going agile I will present the goals I laid out for my small team. These goals are linked to the overall team goals and the overall corporate goals. Defining the reason for going agile and what you hope to accomplish is a very important first step in going agile. Making sure your goals are linked up the hierarchy to overall business goals will help keep the entire team aligned and focused on the same end results.

In addition to goals I included some principles and practices to help achieve each goal. Again, this is overwhelmingly slanted towards the automation team and achieving continuous delivery, but I believe that automation continuous delivery directives that came from corporate was one of the primary drivers of going agile.

Having the entire business invested in agile is very important to actually going agile. Moving an enterprise waterfall team to agile is virtually impossible, in my opinion, without agreement from the individual teams tup to top level executives.

##Increase the amount of value delivered to end users

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
  - Monitor value measures to determine when you are successful

##Increase the flow of value to end users

- Identify, protect, and improve bottlenecks
  - Map value stream
- Decouple the architecture so that build, deploy, test and rollbacks can happen at component level
- Make deployment easy... push button
- Reduce feedback loops
    - Provide continuous feedback for build, deploy and test 
- Measure the flow of value to customers
- Monitor flow measurements to determine when you are successful

##Improve the work experience

- Blameless culture
- Self organized teams
- Improve communication
- Make feedback openly visible