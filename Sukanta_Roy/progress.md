# Sukanta Roy

**Project: Questions+**

Overall Direction:
- [x] MCQ questions:
	- Attach weights to options
	- Calculate more statistics (Total, average)
	- Ensure downloaded data contains all data shown in the page.
- [x] MSQ questions:
	- Attach weights to options
	- Calculate more statistics
	- Ensure downloaded data contains all data shown in the page.
- [x] Rubric questions:
	- Attach weights to each cell instead of each column
	- Update results accordingly
	- Ensure downloaded data contains all data shown in the page.
	- Migrate legacy data into new format
	- Remove legacy code
- [ ] [Add a new question template](https://github.com/TEAMMATES/teammates/issues/8850) -> This feature was put on hold by the organization until the GSoC period ends. For reference: https://github.com/TEAMMATES/teammates/issues/8850#issuecomment-409793711
---

Week 1 Plan:
- [x] Work on [Instructor: edit rubric question: tweak UI to prevent misunderstanding of weights](https://github.com/TEAMMATES/teammates/issues/8824)
- [ ] Implement the backend part of [MCQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/2776)
	- [ ] Update `QuestionDetails` class
	- [ ] Update `Logic` class
	- [ ] Update `Action` class
	- [ ] Add Corrosponding Unit and Integration tests
- [ ] Code review and fix

Week 1 Work:
- [x] Merged: [Instructor: edit rubric question: tweak UI to prevent misunderstanding of weights](https://github.com/TEAMMATES/teammates/issues/8824)

Week 1 Retrospect:

This week the plan was to complete the backend of MCQ weights feature, and I edited `FeedbackMcqQuestionDetails.java` accordingly, but
I forgot to take into account about MCQ `other` option and how weight feature should behave in case of the `Other` option. After discussing with my mentors and Prof. Damith, we came to the conclusion that, at this point, we will add `weight` feature to `other` option too, giving the instructor full flexibility of the feature. We also discussed the best possible way to store the necessary fields in the datastore. In coming weeks, I will have to change my initial implementation of the weight feature to add the feature for the `Other` option. 

Week 2 Plan:
**Final Semester Exams**
- [ ] Finalize the sample question list for the new question template

Week 2 Work:
- [x] Made 3 sample templates to choose from, for the [Add new template](https://github.com/TEAMMATES/teammates/issues/8850) feature.

Week 2 Retrospect:

In week 2, due to my final exams, I was not able to work on my project. But as the plan was to finalize the sample question list for the new template, I made three templates with sample questions to choose from. The plan is to create a template that will focus on one aspect only (e.g. Team dynamics, Performance based questions with no open ended essay questions etc.). Though further discussion is needed with my mentors and Organization admins to finalize one template that will add the most value to teammates and the instructors. Hoping to do it after May 30th, as Prof. Damith will be available after that.

Week 3 Plan:
- [x] Finish implementing the backend part of [MCQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/2776)
- [ ] Implement the frontend part of [MCQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/2776)
	- [ ] Update question template to add the new UI for MCQ weights
	- [ ] Add JS functionalities
	- [ ] Add necessary JS tests
	- [ ] Add frontend UI tests

Week 3 Work:
- [x] Merged: [Instructor: Edit session: Rubric question: Add front-end validation for empty weights](https://github.com/TEAMMATES/teammates/issues/8631)
- [x] Merged: [Rubric question add/edit action test: Add missing parameter and additional tests](https://github.com/TEAMMATES/teammates/issues/8855)
- [x] Finished adding backend implementation for MCQ weights feature in [Instructor: MCQ questions (single answer): support attaching weights to options #2776](https://github.com/TEAMMATES/teammates/pull/8860)

Week 3 Retrospect:
In this week, created the pull request for MCQ weights and added backend for MCQ weights. It took longer than expected to add tests for backend as I am relatively new to Unit testing. Apart from that, no major setbacks.

Week 4 Plan:
- [x] Finish off remaining front-end part from last week
- [x] If frontend and backend part for MCQ weights are finished, then add necessary UI tests and make the PR ready for review.
- [ ] Calculate more statistics for MCQ questions to show in the results page
- [x] Code review and fix

Week 4 Work:
- [x] Added new UI for MCQ weights by updating question templates.
- [x] Attached JS functionalities to it
- [x] Added front-end UI tests to MCQ weights
- [x] Added necessary End-to-End tests for MCQ weights

Week 4 Retrospect:
In this week, I worked on front-end part of MCQ weights and added necessary tests to it. Could not complete the calculation of statistics part within this week as working on JS functionalities and the tests took longer than what I had initially anticipated.

Week 5 Plan:
- [x] Calculate more statistics for MCQ questions to show in the results page
- [x] Merge [Instructor: Results: Use separate result stats templates for MSQ questions instead of re-using MCQ templates](https://github.com/TEAMMATES/teammates/issues/8894) as it is blocking the calcualtion of statistics part.
- [x] Ensure that the CSV files include all data shown in the page for MCQ questions
- [x] Add necessary UI tests for results page for MCQ statistics.
- [x] Update documentation for MCQ questions in the `InstructorHelp` page
- [ ] Implement the backend part of [MSQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/7281)
	- [ ] Update `QuestionDetails` class
- [ ] Code review and fix

Week 5 Work:
- [x] Merge [Instructor: Results: Use separate result stats templates for MSQ questions instead of re-using MCQ templates](https://github.com/TEAMMATES/teammates/issues/8894)
- [x] Added Response Summary and Per Recipient summary for result pages
- [x] Update CSV files to match the content of the result pages for MCQ questions.
- [x] Update InstructorHelp page
- [x] Add UI test for MCQ weights statistics in `FeedbackMcqQuestionUiTest.java`

Week 5 Retrospect:
In this week, I was finishing my work on MCQ weights feature, specifically the Statistics part, and updating the documentation parts. Though I initially thought I would be able to start working on the MSQ weight feature, but couldn't as the statistics part took a little more time than I thought would be sufficient.

Week 6 Plan:
- [x] Implement the backend part of [MSQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/7281)
	- [ ] Add Corrosponding Unit and Integration tests
- [ ] Implement the frontend part of [MSQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/7281)
	- [ ] Update question template to add the new UI for MSQ weights
	- [ ] Add JS functionalities
	- [ ] Add necessary JS tests
	- [ ] Add frontend UI tests
- [ ] If frontend and backend part for MSQ weights are finished, then add necessary UI tests and make the PR ready for review.
- [ ] Update documentation for MSQ questions
- [x] Code review and fix

Week 6 Work:
- [x] Add `Weighted Percentage` instead of `Average` in MCQ stats
- [x] Make changes as suggested in Code Review to make MCQ weight PR merge ready
- [x] Finish the Backend part of MSQ weight feature.

Week 6 Retrospect:
This week I spent most of my time in Code review and fix, and also did the MSQ backend part. Though I am running behind my schedule I am sure to catch my within next week.

Week 7 Plan:
- [x] Implement the frontend part of [MSQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/7281)
	- [x] Update question template to add the new UI for MSQ weights
	- [x] Add JS functionalities
	- [x] Add necessary JS tests
	- [x] Add frontend UI tests
- [x] If frontend and backend part for MSQ weights are finished, then add necessary UI tests and make the PR ready for review.
- [x] Update documentation for MSQ questions
- [x] Calculate more statistics for MSQ questions (Total, average for each student) to show in the results page
- [x] Ensure that the CSV files include all data shown in the page for MSQ questions
- [ ] Code review and fix

Week 7 Work:
- [x] Created PR for MSQ weight feature: [Multiple-choice (multiple answers) questions: support weights for options #7281](https://github.com/TEAMMATES/teammates/pull/8917)
- [x] Finish off front-end part of MSQ weights
- [x] Added UI and end-to-end tests
- [x] Added Response summary and Per recipient summary for MSQ statistics
- [x] Reused MCQ result templates and removed redundant MSQ result templates to finish off [Instructor: Results: Use a common template to generate both MCQ and MSQ result stats](https://github.com/TEAMMATES/teammates/issues/8895) in MSQ PR itself.

Week 7 Retrospect:
This week, I mainly worked on MSQ weights feature and made it review ready. There was no major setbacks in this week.

Week 8 Plan:
- [x] Buffer time to finish off any remaining work from past weeks and for code review and fixes
- [ ] Merge [Instructor: Results: Use a common template to generate both MCQ and MSQ result stats](https://github.com/TEAMMATES/teammates/issues/8895)

Week 8 Work:
- [x] Code Review and Fix
- [x] Added the fix for [Instructor: Results: Use a common template to generate both MCQ and MSQ result stats](https://github.com/TEAMMATES/teammates/issues/8895) in [Multiple-choice (multiple answers) questions: support weights for options #7281](https://github.com/TEAMMATES/teammates/pull/8917) PR instead of submitting a separate PR.

Week 8 Retrospect:
This week was mostly spent on MSQ weights PR's code review and fix. We stumbled upon a small roadblock this week, where me and my mentors mistakenly thought that we no longer support the `None of the Above` option in MSQ question, and to find out if the legacy data was migrated or not I had to write a migration script, but as I am not very familiar with `Objectify`, it took me a lot of time to learn about it. But later we realised that we still support the `None of the Above` option for MSQ questions and that is why the data migration never happened. It was my novice mistake to not check first before jumping on to write the migration script as it took a lot of valuable time, but on the positive side it helped me become familiar with the `Objectify` API which I will anyway need for Rubric question's data migration.

Week 9 Plan:
- [ ] Implement the backend for [Rubric questions: allow weightages for sub questions](https://github.com/TEAMMATES/teammates/issues/7224)
	- [x] Update `QuestionDetails` class
	- [ ] Update `Logic` class
	- [ ] Update `Action` class
	- [ ] Add Corrosponding Unit and Integration tests
- [x] Code review and fix
- [ ] Implement the frontend for [Rubric questions: allow weightages for sub questions](https://github.com/TEAMMATES/teammates/issues/7224)
	- [ ] Update question template to add weights on each cell

Week 9 Work:
- [x] Code Fix for [Multiple-choice (multiple answers) questions: support weights for options #7281](https://github.com/TEAMMATES/teammates/pull/8917)
- [x] Submitted PR for [Student: submit responses: implement back-end integrity check for responses #2542](https://github.com/TEAMMATES/teammates/pull/8956)
- [x] Updated Rubric `QuestionDetails` class to add required methods needed to support Rubric weights for each cell.

Week 9 Retrospect:
This week I fell behind schedule a big time, as initially I was very confused on how to write code that will both work on legacy data and new data, for that I created a demo branch to try and test what will work and what may not. This took a lot of time and I fell behind my schedule. At the end of this week I submitted the [Rubric weight PR](https://github.com/TEAMMATES/teammates/pull/8961).

Week 10 Plan:
- [ ] Implement the backend for [Rubric questions: allow weightages for sub questions](https://github.com/TEAMMATES/teammates/issues/7224)
	- [x] Update `Logic` class
	- [x] Update `Action` class
	- [x] Add Corrosponding Unit and Integration tests
- [ ] Implement the remaining frontend part of Rubric questions weights for each cell
	- [x] Update question template to add weights on each cell
	- [ ] Add JS functionalities
	- [ ] Add JS tests
	- [ ] Add Partial UI tests (Only the frontend part)
- [ ] If frontend and backend part are finished, then add necessary UI tests (with backend validations) and make the PR ready for review.
- [x] Code review and fix

Week 10 Work:
- [x] Completed Rubric backend part
- [x] Modified Rubric form to add weight fields for each cell
- [x] Code Review and Fix for [Student: submit responses: implement back-end integrity check for responses #2542](https://github.com/TEAMMATES/teammates/pull/8956)
- [x] Merged [Multiple-choice (multiple answers) questions: support weights for options #7281](https://github.com/TEAMMATES/teammates/pull/8917)
- [x] Fixed [Instructor: Results: Use a common template to generate both MCQ and MSQ result stats](https://github.com/TEAMMATES/teammates/issues/8895)

Week 10 Retrospect:
This week I completed Rubric backend part and also modified rubric form to support weights for each cell. MSQ weight PR was approved this week and was merged into the `master` branch.

Week 11 Plan:
- [x] Implement the remaining frontend part of Rubric questions weights for each cell
	- [x] Add JS functionalities
	- [x] Add Partial UI tests (Only the frontend part)
- [x] If frontend and backend part are finished, then add necessary UI tests (with backend validations) and make the PR ready for review.
- [x] Modify Rubric statistics page
- [x] Update documentation for Rubric question in the `InstructorHelp` page.

Week 11 Work:
- [x] Completed the front-end part Rubric weights
- [x] Modified Rubric Statistics page
- [x] Updated `InstructorHelp` page.
- [x] Code Review and fix for [Student: submit responses: implement back-end integrity check for responses #2542](https://github.com/TEAMMATES/teammates/pull/8956)
- [x] Wrote a script to check if the datastore has questions with negative weights so that we can decide whether to support negative weights or to block it.

Week 11 Retrospect:
This week I made Rubric weights PR review ready. We faced a problem this week where we had to decide whether we should continue to support negative weights for rubric questions or should we block negative weights as negative weights make the `Weighted Percentage` stats useless. For that I wrote a script to check how many questions have negative weights and based on the results of that script we decided to exclude `Weighted Percentage` from Rubric questions, as there are questions with negative weights in the production indicating that it is an used feature which we should not remove. Other than this there were no major roadblocks this week.

Week 12 Plan:
- [ ] Finalize the set of questions that will be added as a template
- [ ] Implement the backend part of the new question template
- [x] Code review and fix
- [x] Write data migration script to convert 1D weight list to 2D list for Rubric weights feature.

Week 12 Work:
- [x] Code review fix for Rubric Weights Feature
- [x] Created issue and submitted PR for the bug: [instructorFeedbackResultsPage: Team Contribution Question: Help link is not showing statistics table](https://github.com/TEAMMATES/teammates/pull/9006)
- [x] Submitted PR for [Rubric questions: allow weight for each cell: Migrate legacy data into new format #9007](https://github.com/TEAMMATES/teammates/pull/9008)
- [x] Submitted PR for [FeedbackNumericalScaleQuestionDetails: refactor long methods #6657](https://github.com/TEAMMATES/teammates/pull/9020)

Week 12 Retrospect:
This week I mainly devoted my time in making the Rubric weights PR merge ready and wrote the data migration script for the step 2 of the data migration process which is to migrate the legacy data into new format. The new question template feature [Instructor: Feedback Session: Add a new session template with sample questions](https://github.com/TEAMMATES/teammates/issues/8850) was put on hold until GSoC period ended.

Week 13 Plan:
- [ ] Finish off any remaining work from last week
- [ ] Implement the frontend part of the new question template
- [ ] Update documentation
- [ ] Code review and fix
- [x] Remove legacy code that deals with old format weights for rubric weights feature

Week 13 Work:
- [x] Created issue and submitted PR for [Rubric questions: allow weight for each cell: Remove legacy code](https://github.com/TEAMMATES/teammates/issues/9026)
- [x] Merged [Rubric questions: allow weight for each cell](https://github.com/TEAMMATES/teammates/pull/8961)

Week 13 Retrospect:
This week I submitted PR to remove the legacy code in Rubric weights feature, which is the final step of data migration process. The PR is `onHold` as the data migration process in not complete yet. Hoping to complete the data migration and also merge this PR within the next week. There was no major setbacks in this week.

Week 14 Plan:
- [ ] Buffer time for review and iterations
