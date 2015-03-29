#Sprinting

I won't go into what a sprint is because it is common knowledge in the software industry and there is tons of resources about it online. When I joined the team they were already sprinting. We went through various evolutions as we moved from a more waterfall based sprint to a more agile sprint.

##Sprint Planning

###v1.0

In the beginning we had no real team planning. Tickets were assigned by the development manager and the developers completed the tickets. The development manager and product manager would plan sprints in closed door meetings. Then the development manager would consult with the tech manager for estimations. The development manager and tech lead met with developers to discuss the development plan (architecture, design...).

We had daily standups or Scrum to review status, but it was more of a status meeting for the development manager than an effective tool to build team work and accelerate the flow of work.

###v2.0

Going agile we switch to a more team approach to sprint planning. 

####Requirements Review

Before the start of each sprint the delivery team convenes to plan the sprint. The first meeting is a requirement review. In the requirement review, the team discusses the requirements and break out tickets. How this is done is not really important as long as the team agrees on the break out. 

We try to break out tickets so that they are large enough for at least a days work for one developer. If a ticket is larger than a few days it should be broken down into sub tickets. 

Each ticket should also be testable on some level. Either by a unit test, API test, or UI test. If the ticket is for creating database objects, configuration or infrastructure changes, or other non-code change, the test would be a visual inspection or preferably by some means of automatically testing the change.

The sprint lead will direct the meeting and make sure the discussion doesn't get bogged down by deep, specific, discussions of the technical details of the ticket. During the meeting the sprint lead will keep track of the tickets by writing the ticket title on a "sticky" and slapping it on the wall. 

The scribe will keep a document outlining what was discussed and open questions. The scribe will deliver the notes to the team after each meeting. 

Open questions will be handled by the analysts who is responsible for getting the answers.

Once the team has gone through the entire requirements document the sprint lead will add the tickets to the ticket management system.

####Estimation

The next sprint planning meeting is to get a consensus on the acceptance criteria and estimate for the tickets. The sprint lead will again drive the meeting and will update the ticket in the ticket system with acceptance criteria and estimate. The lead brings up the ticket system on a projector and the team discussion each ticket. The sprint lead will do a quick review of the ticket and a discussion ensues on what is believed to be delivered by the ticket. Once the lead feels the team is at a point to make a decision, the lead will write the acceptance criteria and ask the team for agreement. The team will weigh in and the lead will change as necessary until the entire team agrees. Then the lead will ask for estimates. This could be planning poker or other estimate technique, but having the team just shout out estimates works too. Again, once an agreement is met on the estimate it is recorded on the ticket. 

The sprint lead will review the estimates with the development manager to plan the sprint capacity. The development manager will meet with product management to get sign off on the acceptance criteria, estimate, and capacity plan. Once an agreement is achieved the managers will agree on a sprint schedule. Generally, the schedule gives dates for start development, end development, sprint demo, deployment to UAT, deployment to production. After the management green lights the sprint development can commence on the scheduled date.