To simplify the movement of cards, we want to automate the moving of work items. Work items can be moved when various event occur on the ALM server \(\#NoCardMove\). This depends on 

* All development occurring on short-lived \(e.g. 1-3 days\) feature/work item/user story branches. 
* Branches are merged to master on pull request only. 
* Pull requests are built and tested before merging. 
* All projects have a test stage where the public API is exercised against a mock to verify acceptance criteria. 
* There is a Test, UAT, Stagging, and Production environment that are continuously delivered to.

We monitor events in the ALM. When the ALM doesn't support publishing events or providing web hooks we look for ways to trigger an event. If a build server doesn't publish events, we could write a task that we include as the last task in the build that will post an event to an API that can handle the event and move the card.

These are the events I envision:

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

Move work item to:

* Development and assigned to branch creator when branch created.
* Verification doing and assigned to pull request creator when pull request created.
* Verification done when pull request succeeded.
* Validation doing when test started.
* Validation done when test succeeded.
* UAT doing when release to UAT environment succeeded.
* Release doing when release to stagging environment succeeded.
* Work item in Release done when release to production environment succeeded.

On failure, a bug is created, assigned to process owner, and linked to failing work item. Only one bug per failure is created, no duplicates. If multiple work items are included in a failure, link all related work items \(e.g. release fails while releasing multiple work items\).

Cancel is user initiated stop of process. Abort is system initiated stop of process \(e.g. timeout\).

{tfsUrl}/{collection}/{project}/\_apps/hub/ms.vss-servicehooks-web.manageServiceHooks-project

Use ocelot gateway like envoy, itsio, ambassador, and statsd. A .Net Core sidecar to provide unobtrusive observability of running containers.

