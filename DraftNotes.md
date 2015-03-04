v1.0:

1 product manager
1 development manager
1 tech lead
5 developers
1 development QA
2 QA (part time)

Product manager provides requirements document with detailed specs and Photoshop mockups.

SVN source control with branched main repo. Development for each planned release starts with a branch of the previous branch and all developers work off of the same branch. After each release, the branch is merged to the next branch and merged back into trunk. There can be multiple branches in development at one time, but usually not more than 2. Periodically, the oldest active branch is merged its child branch.

Developer code review in SVN tool.

Automated nightly build.

Automated nightly deploy to development environment.

Manual deploy to UAT and production environment.

Manual testing of release changes in development environment by the development QA.

Manual testing of release changes by QA in UAT environment.

Manual regression test of release by QA in UAT environment.

Manual deployment validation of release by QA in production.

No metrics on any aspect of the pipeline.

v2.0

1 product manager
1 development manager
1 tech lead
6 developers
1 junior developer
2 QA (part time)

Development QA was integrated into the QA team and developers had to take on the role of manually testing the release in the development environment.

Junior developer tasked with creating automated tests for one of the applications.

v3.0
1 product manager
1 development manager
1 tech manager
4 developers
2 automation engineers
1 database administrator
4 QA (part time)

Development moved 1 developer to focus totally on production support and one to help with customer implementations and they are not counted in the headcount above.

Automation team formally organized and focused on creating the testing framework and building out the continuous delivery environment. The automation team also focused on development operations in that they led the effort to implement infrastructure as code. Lastly, the automation took over manually testing in the development environment.

Database administrator focuses on revamping database operations from scripting, architecture, monitoring, performance...



Before the start of each sprint the delivery team convenes to plan the sprint. The first meeting is a requirement review. In the requirement review, the team will discuss the requirements and break out tickets. How this is done is not really important as long as the team agrees on the break out. 

We try to break out tickets so that they are large enough for at least a days work for one developer. If a ticket is larger than a few days it should be broken down into sub tickets. 

Each ticket should also be testable on some level. Either by a unit test, API test, or UI test. If the ticket is for creating database objects, configuration or infrastructure changes, or other non-code change, the test would be a visual inspection or preferably by some means of automatically testing the the change.

The sprint lead will direct the meeting and make sure the discussion doesn't get bogged down by deep, specific, discussions of the technical details of the ticket. During the meeting the sprint lead will keep track of the tickets by writing the ticket title on a "sticky" and slapping it on the wall. 

The scribe will keep a document outlining what was discussed and open questions. The scribe will deliver the notes to the team after each meeting. 

Open questions will be handled by the analysts who is responsible for getting the answers.

Once the team has gone through the entire requirements document the sprint lead will add the tickets to the ticket management system.

The next sprint planning meeting is to get a consensus on the acceptance criteria and estimate for the tickets. The sprint lead will again drive the meeting and will update the ticket in the ticket system with acceptance criteria and estimate. The lead brings up the ticket system on a projector and the team discussion each ticket. The sprint lead will do a quick review of the ticket and a discussion ensues on what is believed to be delivered by the ticket. Once the lead feels the team is at a point to make a decision, the lead will write the acceptance criteria and ask the team for agreement. The team will weigh in and the lead will change as necessary until the entire team agrees. Then the lead will ask for estimates. This could be planning poker or other estimate technique, but having the team just shout out estimates works too. Again, once an agreement is met on the estimate it is recorded on the ticket. 

The sprint lead will review the estimates with the development manager to plan the sprint capacity. The development manager will meet with product management to get sign off on the acceptance criteria, estimate, and capacity plan. Once an agreement is achieved the managers will agree on a sprint schedule. Generally, the schedule gives dates for start development, end development, sprint demo, deployment to UAT, deployment to production. After the management green lights the sprint development can commence on the scheduled date. 

Acceptance Tests are ran throughout the day a scheduled times. Acceptance tests are tagged with ticket number. The automated acceptance tests will parse the change set for ticket numbers and will add the numbers as test tags to the command line that controls what tests to run. The test runner is smart enough to take the test tags from the command line and run only those tests that have a tag matching the ticket number. It is vital that each check-in has an associated ticket number. There should be a pre-commit check that verifies that the ticket includes the ticket number. If the team isn't diligence about adding ticket numbers, tests won't run for the check-in and this puts the ticket in jeopardy. So, it should be carefully guarded during code review.

Release tests are ran nightly. Acceptance Tests are also tagged with the release they are scheduled to deploy with. Nightly all of the release tagged tests are ran so we have a daily indication of what tests are passing or failing.

We also run regression tests nightly. Regression tests are acceptance tests with additional scenarios to cover additional criteria.

Testing quality takes precedence over developing functionality. Testing security takes precedence over testing quality. Testing is basically attempting to disprove a theory that a feature works, is secure, is performant...etc.