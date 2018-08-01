# Shradheya Thakre

**Project: Coverage Boost**

Overall Direction:
- Reduce Technical Debt (Upgrade to Selenium 3.x)
- Update test cases to optimize CI Build process
- Add more test cases for missing features
- Improving test infrastructure: Make it easier to write new tests, make tests less fragile, make test code easier to understand
- Explore new JavaScript testing framework to replace QUnit

---

Week 1 Plan:
- [x] Review PR #8813 [FeedbackRankQuestionUiTest.json: Fix data for Tests #8794 #8813](https://github.com/TEAMMATES/teammates/pull/8813)
- [x] Review PR #8770 [Add AdminExceptionTestActionTest #6902 #8770](https://github.com/TEAMMATES/teammates/pull/8770)
- [ ] Resolve minor issues to improve testing
  - [ ] [Resolve Firefox 46.0.1 styling issue #8763](https://github.com/TEAMMATES/teammates/issues/8763)
  - [x] [Remove JS Coverage requirement #8768](https://github.com/TEAMMATES/teammates/issues/8768)
- [x] Investigate which tests need to be modified

Week 1 Work:

- [x] Reviewed PR #8813 [FeedbackRankQuestionUiTest.json: Fix data for Tests #8794 #8813](https://github.com/TEAMMATES/teammates/pull/8813)
- [x] Reviewed PR #8770 [Add AdminExceptionTestActionTest #6902 #8770](https://github.com/TEAMMATES/teammates/pull/8770)
- [x] Merged PR: [Remove JS Coverage requirement #8768](https://github.com/TEAMMATES/teammates/issues/8768)

Week 1 Retrospect:

Due to other commitments for the entire week, I wasn't able to put in enough time to write any tests. Hence I spent the time in investigating what tests should be added/modified. I think this time paid off as I was able to catch up for this week by creating multiple PR's for the pre existing issues in the following week.

I also spent the week in reviewing the Testing related PR's which were pending for a long time and some of which were blocking other PR's from getting merged(Eg. #8813)


Week 2 Plan:
- [x] Adding more Test cases based on `TODO` present in Testing code (Issues will be created accordingly)
  - [x] [BackDoorTest: add test for deletion of Feedback Session](https://github.com/TEAMMATES/teammates/issues/8842)
  - [x] [Testing: Improve instructions and process #8844](https://github.com/TEAMMATES/teammates/issues/8844)
- [x] Review PR's related to Testing which have been left untouched for a long time

Week 2 Work:

- [x] Fixed Critical Bug unrelated to initial project proposal. Merged PR: [Instructor: view results: fix bug: sorting results by team is broken](https://github.com/TEAMMATES/teammates/pull/8840)
- [x] Merged PR: [BackDoorTest: add test for deletion of Feedback Session](https://github.com/TEAMMATES/teammates/pull/8843)
- [x] Authored 3 other PR

Week 2 Retrospect:

During this week I created 4-5 PR's related to testing however only few were merged due to the time taken to review PR's. Hence I will be devoting Week 3 to ensure all open PR's are reviewed and merged.

I think the review process slowed me down but also it let me catch up on the work that needed to be done in Week 1.

Week 3 Plan:
- [x] Research  work on Upgrade to Selenium 3.x
- [x] Code Review and Fix
- [x] Work on improving stability of Tests

Week 3 Work:

- [x] Set up the initial Selenium upgrade
- [x] Updated currently ongoing PR's based on review. #8845 #8891 and #8862
- [x] Reviewed PR's of existing and new contributors. #8846 and #8881
- [x] Investigated issues of problems arising in build and testing process. E.g. `AdminHomePageUiTest` and `InstructorStudentListPageUiTest`
- [x] Fixed issue of instability of `SHomeUiT` and `SProfileUiT` which has reduced the build time

Week 3 Retrospect:

During this week I worked on initial set up for the Selenium 3.8 upgrade, however I have currently put it on pause as based on fixing a few tests, I realised that the build process will be eventually 40+ mins with the new geckodriver. Hence, I started working on improving stability of tests. This week I have fixed for `SHomeUiT` and `SProfileUiT` which has PR still in review process.

Week 4 Plan:
- [ ] Start work on Upgrade to Selenium 3.x
- [x] Work on improving stability of UI Tests

Week 4 Work:

- [x] Reviewed PR's of contributors (#8849) and helped resolve queries (#8861)
- [x] Researched on JS Unit testing frameworks
- [x] Investigated about more unstable tests

Week 4 Retrospect:

This week I focused more on learning Testing in-depth. It was mainly because in order to improve stability of tests, I needed to be sure that what I was doing actually worked and figuring out what was the reason of instability.
Other than my own project, I also focused on other duties like helping other contributors with the problems that they faced in tests/build process. This helped me in finding more problems and working on solving them in future.

Week 5 Plan:
- [ ] Refactor `FeedbackRubricQuestionUiTest` and `FeedbackRankQuestionUiTest`
- [x] Continue unfinished work from previous week

Week 5 Work:

- [x] Work on post-release issue problems related to testing #8910 and #8911
- [x] Find the Appveyor build issue and review the PR which fixed it #8913
- [x] Continue making requested changes based on reviews

Week 5 Retrospect:

This week due to post release issues related to testing, I spent most of my time fixing them rather than working on the project plan as they were of higher priority. However, I plan to use the buffer's in future weeks to complete the work that I planned to finish this week.

Week 6 Plan:
- [x] Buffer week to complete unfinished work and investigate more on where testing needs to be improved

Week 6 Work:

- [x] Buffer week to complete unfinished work and investigate more on where testing needs to be improved
- [x] Reviewing PR's by contributor
- [x] Management work for TEAMMATES
- [x] Helping other contributor with queries and figuring out how to solve issues for developers
- [x] Continue making requested changes based on reviews

Week 6 Retrospect:

This week as planned was left to complete left over work and work on reviews provided by mentors. This buffer time helped in finishing old PR's and merge them.

Week 7 Plan:
- [x] Add more tests for ~`InstructorSearchPage`~ and similar files
- [x] Refactor more testing code and improve stability

Week 7 Work:

- [x] Refactor more testing code and improve stability
- [x] Merged PR: FeedbackRankQuestionUiTest.json: Fix data for Tests #8794
- [x] Merged PR: Add test for scrolling function
- [x] Merged PR: InstructorCourseDetailsPageUiTest: testing on live server: increase success rate for checking email delivery #7788

Week 7 Retrospect:

Some tests which are untable have been fixed and have ongoing PR with minor changes left to be made before they can be merged. These took long to merge as it took time to understand the reasoning and ensure that they become stable after using the workaround. In future more PR's of similar kind will be made to improve stability.

Week 8 Plan:
- [x] Investigate on why certain tests require to be run extra time to pass
- [x] Improve stability of fragile tests

Week 8 Work:

- [x] Work on testing errors on live production server
- [x] Fix assertion error in instructorCourseJoinEmail on live server #8452
- [x] EmailGeneratorTest failing on live server #8908

Week 8 Retropect:

This week was devoted to fix urgent bugs and testing issues on live server.

Week 9 Plan:
- [x] Based on various Bug reports, find out how to add more tests which can spot bugs while testing
- [ ] Explore new Testing Framework for JS which can be useful for front end migration

Week 9 Work:
- [x] Merge [InstructorFeedbackResultsPageUiTest: Improve testing logic and procedure #8858](https://github.com/TEAMMATES/teammates/pull/8859)
- [x] Merge [Remove wrong Godmode changes due to unstable test #8937](https://github.com/TEAMMATES/teammates/pull/8938)
- [x] Investigate tests failing on live server

Week 9 Retrospect:

This week was spent on making requested changes based on reviews for the already open PR's. Some administrative work was also done for e.g. making PR to correct unnecessary changes and reviewing and merging PR.

Week 10 Plan:
- [x] Buffer time to do unfinished work

Week 10 Work:
- [x] Review PR: [InstructorHomePageUiTest & InstructorCoursesPageUiTest failing on 'recycling-bin' branch #8971](https://github.com/TEAMMATES/teammates/pull/8973)
- [x] Merge PR: [AdminActivityLogPageAction: fix bug in generation of status message #6711](https://github.com/TEAMMATES/teammates/pull/8970)

Week 10 Retrospect:

Continued working on the review loop of existing PR's. Also reviewed 3-4 PR's of other contributors and got them merged. A PR of bug fix which was left untouched for a while was resolved.

Week 11 Plan:
- [ ] Work on [Issue #4034](https://github.com/TEAMMATES/teammates/issues/4034)

Week 11 Work:
- [x] Merge PR: [ProfilesDbTest.testUpdateStudentProfile failing on live server #8958](https://github.com/TEAMMATES/teammates/pull/8966)
- [x] Review PR: [Instructor: comment on responses: support entering comments for each response from view RQG #8987](https://github.com/TEAMMATES/teammates/pull/8992)
- [x] Review PR: [Instructor: Feedback Session: question number drop down menu #8942](https://github.com/TEAMMATES/teammates/pull/8949)
- [x] Review PR: [Instructor: Question view: visibility icon does not appear for new comments #8899](https://github.com/TEAMMATES/teammates/pull/8934)

Week 11 Retrospect:

This week was mainly spent on reviewing the critical PR's of other contributors and working on open PR's. Some post release issues were solved this week. There was deviation from the work plan here because the issue of greater priority was popped up this week.

Week 12 Plan:
- [ ] Add Tests: [Create Unit Tests for Feedback*QuestionDetails classes#1501](https://github.com/TEAMMATES/teammates/issues/1501)
- [ ] Complete PR's which were delayed from previous weeks

Week 13 Plan:
- [ ] More details to be added later depending on the priority
- [ ]
- [ ]

Week 14 Plan:
- [ ] More details to be added later depending on the priority
- [ ]
- [ ]
