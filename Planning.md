# Planning

## Release Planning

### v1.0

When I began there was a release every few months. The items in the release were decided in a closed door meeting between the product and development manager. Releases had hard deadlines that were not very flexible. Everything planned in the release was expected to be in the release before it could be delivered \(not very agile\).

### v2.0

Going agile, we moved to team release planning. Releases are planned by the full team in an all hands quarterly meeting. In the release planning meeting we review the backlog as a team. The product manager gives a brief overview of each item in the backlog and sets the priority for them. The team agrees on what release to align the prioritized items under.

Then the releases are set on a monthly schedule that consists of 2 sprints. By the end of the 1-2 hour meeting the releases for the next quarter are scheduled. This is still waterfall'ish in my opinion, but we got rid of the infexibility and hard deadlines. It was no longer a bad thing to extend a deadline or remove an item from a release as long as it wasn't expected by a customer or affected an external agreement.

There was no magic formula to making this agile transition. The product and development manager said this is the way and the team made it so. Surprisingly, the product didn't suddenly fall on its face. We were able to keep the release schedules while maintaining release quality. In the end we increased the amount and flow of value to end users, while improving the work experience by instilling a feeling of product ownership throughout the entire team.

## Sprint Planning

I won't go into what a sprint is. It is common knowledge in the software industry and there are tons of resources about it online. When I joined the team they were already sprinting. We went through various evolutions as we moved from a more waterfall based sprint to a more agile sprint.

### v1.0

In the beginning we had no real team planning. Tickets were assigned by the development manager and the developers completed the tickets. The development manager and product manager would plan sprints in closed door meetings. Then the development manager would consult with the tech manager for estimations. The development manager and tech lead met with developers to discuss the development plan \(architecture, design...\).

We had daily stand-ups or Scrum to review status, but it was more of a status meeting for the development manager than an effective tool to build team work and accelerate the flow of work.

### v2.0

Going agile we switch to a more team approach to sprint planning.

Before the start of each sprint the delivery team convenes to plan the sprint. The first order of business is to select a sprint lead. The sprint lead will be responsible for the sprint, running the sprint meetings and scrum, also the leader will be the developer left behind to support the sprint as it moves to production and the rest of the sprint team moves on to the next sprint.

#### Requirements Review

The first meeting is a requirement review. In the requirement review, the team discusses the requirements and break out tickets. How this is done is not really important as long as the team agrees on the break out.

We try to break out tickets so that they are large enough for at least a days work for one developer. If a ticket is larger than a few days it should be broken down into sub tickets.

Each ticket should also be testable on some level. Either by a unit test, API test, or UI test. If the ticket is for creating database objects, configuration or infrastructure changes, or other non-code change, the test would be a visual inspection or preferably by some automated means of testing the change.

The sprint lead will direct the meeting and make sure the discussion doesn't get bogged down by deep, specific, discussions of the technical details of the ticket. During the meeting the sprint lead will keep track of the tickets by writing the ticket title on a "sticky" and slapping it on the wall.

The scribe will keep a document outlining what was discussed and open questions. The scribe will deliver the notes to the team after each meeting.

Open questions will be handled by the analysts who is responsible for getting the answers.

Once the team has gone through the entire requirements document the sprint lead will add the tickets to the ticket management system.

#### Estimation

The next sprint planning meeting is to get a consensus on the acceptance criteria and estimate for the tickets. The sprint lead will again drive the meeting and will update the ticket in the ticket system with acceptance criteria and estimate. The lead brings up the ticket system on a projector and the team discussion each ticket. The sprint lead will do a quick review of the ticket and a discussion ensues on what is believed to be delivered by the ticket. Once the lead feels the team is at a point to make a decision, the lead will write the acceptance criteria and ask the team for agreement. The team will weigh in and the lead will change as necessary until the entire team agrees. Then the lead will ask for estimates. This could be planning poker or other estimate technique, but if your team is honest and works well together, having the team just shout out estimates works too. Again, once an agreement is met on the estimate it is recorded on the ticket.

The sprint lead will review the estimates with the development manager to plan the sprint capacity. The development manager will meet with product management to get sign off on the acceptance criteria, estimate, and capacity plan. Once an agreement is achieved the managers will agree on a sprint schedule. Generally, the schedule gives dates for start development, end development, sprint demo, deployment to UAT, deployment to production. After the management green lights the sprint development can commence on the scheduled date.

