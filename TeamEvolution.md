#Team

In software development "team" is an overloaded term. It could be a two person team like the automation team I am currently on. It could mean the product team, development team, engineering team... etc. 

When I speak of team I like to think of a product delivery team. The product being some sort of software product. I consider a product team as two or more people organized to deliver software. There are many roles that need to be covered on the product delivery team and many times one person can serve in multiple roles.

##Roles

In my experience there have been roles for:

* Product Manager - manages product's business direction and priorities
* Business Analyst - designs product specifications
* Development Manager -  manages product's technical direction and priorities
* Technical Lead - designs product architecture
* Developer - develops product
* Risk Analyst - assesses product risks
* Infrastructure - manages product release and infrastructure

Of course these can be defined simpler or more granularity, but this has fit my experience well. I guess the point in all this is that roles don't really matter as long as the team understands who does what.

##Communication

When going agile team communication is at the heart of successful implementation of an agile methodology. From cross team discussions to plan sprints to delivering feedback at various steps in the delivery pipeline, a team that can communicate will be much more effective and efficient in delivering value.

Does a team need to be co-located to communicate effectively? I don't think co-location is a necessity, but I would assume that there are situation where it is best. I haven't been in that situation, but there has always been a "traditional" rule that says the team must work in the same office to be effective. This is just my personal opinion. Most meetings I go to could have been done virtually, not only done but done more effectively with the quality of communication tools today. Having worked in an open format office, distraction is an issue. At times its great to be able to shout over a desk to talk to someone, but many times useless dialog is the result. Yet, there are people who feel the distractions and useless dialog are instrumental in building team cohesion. Being an introvert I obviously disagree.

##My Team Evolution

My current product team has gone through multiple organizational changes over the past few years. This has been in response to growing business demands and a desire to go agile. Below is an overview of various iterations of the team structure.

###v1.0

####Roles

* 1 product manager (VP)
* 1 development manager
* 1 tech lead
* 5 developers
* 1 development QA
* 2 QA (part time)

####Description

* Product manager provides requirements document with detailed specs and Photoshop mockups.
* SVN source control with branched main repo. Development for each planned release starts with a branch of the previous branch and all developers work off of the same branch. After each release, the branch is merged to the next branch and merged back into trunk. There can be multiple branches in development at one time, but usually not more than 2. Periodically, the oldest active branch is merged to its child branches.
* Developer code review in SVN tool.
* Automated nightly build.
* Automated nightly deploy to development environment.
* Manual deploy to UAT and production environment.
* Manual testing of release changes in development environment by the development QA.
* Manual testing of release changes by QA in UAT environment.
* Manual regression test of release by QA in UAT environment.
* Manual deployment validation of release by QA in production.
* No metrics on any aspect of the pipeline.

###v2.0

####Roles

* 1 product manager (VP)
* 1 development manager
* 1 tech lead
* 6 developers
* 1 junior developer
* 2 QA (part time)

####Description

* Development QA was integrated into the QA team and developers had to take on the role of manually testing the release in the development environment.
* Junior developer tasked with creating automated tests for one of the applications.

###v3.0

####Roles

* 1 product manager (VP)
* 1 business analyst
* 1 development manager (VP)
* 1 tech manager
* 4 developers
* 2 automation engineers
* 1 database administrator
* 4 QA (part time)

####Description

* Development manager promoted to VP
* Development moved 1 developer to focus totally on production support and one to help with customer implementations and they are not counted in the headcount above.
* Product manager added a business analyst who is responsible for creating specs and moved to less detailed Photoshop laced specs to more strategic direction based specs and joint formulation of acceptance criteria with the entire delivery team.
* Automation team formally organized and focused on creating the testing framework and building out the continuous delivery environment. The automation team also focused on development operations in that they led the effort to implement infrastructure as code. Lastly, the automation took over manually testing in the development environment.
* Database administrator focuses on revamping database operations from scripting, architecture, monitoring, performance...
 
###v4.0

####Roles

* Same as v3.0 team

####Description

* Tech lead promoted to development manager
* 1 of the automation engineers promoted to lead
* QA team formally assigned and organized under development