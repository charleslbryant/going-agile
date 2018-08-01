To simplify the movement of cards, we want to automate the moving of work items. Work items can be moved when various event occur on the ALM server \(\#NoCardMove\). This depends on all development occuring on short-lives \(e.g. 1-3 days\) feature/work item/user story branches. Branches are merged to master on pull request only. Pull requests are built and tested before merging. All projects have a test stage where the public API is excersised against a mock to verify acceptance criteria. There is a Test, UAT, Stagging, and Production environment.

* Branch Created
* Pull  Request Created
* Pull Request Succeeded
* Pull Request Failed
* Pull Request Cancelled
* Pull Request Aborted
* Build Started
* Build Succeeded
* Build Failed
* Build Cancelled
* Test Started
* Test Succeeded
* Test Failed
* Test Cancelled
* Test Aborted
* Release Started
* Release Succeeded
* Release Failed
* Release Cancelled

Work item in development and assigned to branch creator when branch created.

Work item in verification doing and assigned to pull request creator when pull request created.

Work item in verification done when pull request succeeded.

Work item in validation doing when test started.

Work item in validation done when test succeeded.

Work item in UAT doing when release to UAT environment succeeded.

Work item in Release doing when release to stagging environment succeeded.

Work item in Release done when release to production environment succeeded.

Bugs are created and assigned to process owner on failure, only one per work item, no duplicates. If we failed the build today, only need one build bug in WIP for the work item.

Cancel is user initiated stop of process.

Abort is system initiated stop of process \(e.g. timeout\).

{tfsUrl}/{collection}/{project}/\_apps/hub/ms.vss-servicehooks-web.manageServiceHooks-project

Use ocelot gateway like envoy, itsio, ambassador, and statsd

