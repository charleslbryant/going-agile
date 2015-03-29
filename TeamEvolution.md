#Team



##My Team Evolution

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