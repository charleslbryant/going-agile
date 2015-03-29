#Testing

##Acceptance Test
Acceptance Tests are ran throughout the day a scheduled times. Acceptance tests are tagged with ticket number. The automated acceptance tests will parse the change set for ticket numbers and will add the numbers as test tags to the command line that controls what tests to run. The test runner is smart enough to take the test tags from the command line and run only those tests that have a tag matching the ticket number. It is vital that each check-in has an associated ticket number. There should be a pre-commit check that verifies that the ticket includes the ticket number. If the team isn't diligence about adding ticket numbers, tests won't run for the check-in and this puts the ticket in jeopardy. So, it should be carefully guarded during code review.

#Release Test
Release tests are ran nightly. Acceptance Tests are also tagged with the release they are scheduled to deploy with. Nightly all of the release tagged tests are ran so we have a daily indication of what tests are passing or failing.

##Regression Test
We also run regression tests nightly. Regression tests are acceptance tests with additional scenarios to cover additional criteria.

##Development Focus
Much like the effort to invert the testing triangle, we had to begin to invert the focus in regards to adding features, quality and security. At first adding features and changes was the most important aspect of our delivery. Testing was second and would suffer in the name of adding features. Security was an after thought and only came up periodically during penetration testing and annual security training for developers. Testing quality takes precedence over developing functionality. Testing security takes precedence over testing quality. Testing is basically attempting to disprove a theory that a feature works, is secure, is performant...etc. Testing security has to be the most important aspect as our customers trust us to keep their information private and secure especially since we are in the financial industry.