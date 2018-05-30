# Sukanta Roy

**Project: Questions+**

Overall Direction:
- MCQ questions:
	- Attach weights to options
	- Calculate more statistics (Total, average)
	- Ensure downloaded data contains all data shown in the page.
- MSQ questions:
	- Attach weights to options
	- Calculate more statistics
	- Ensure downloaded data contains all data shown in the page.
- Rubric questions:
	- Attach weights to each cell instead of each column
	- Update results accordingly
	- Ensure downloaded data contains all data shown in the page.
- [Add a new question template](https://github.com/TEAMMATES/teammates/issues/8850)
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
- [ ] Finish implementing the backend part of [MCQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/2776)
- [ ] Implement the frontend part of [MCQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/2776)
	- [ ] Update question template to add the new UI for MCQ weights
	- [ ] Add JS functionalities
	- [ ] Add necessary JS tests
	- [ ] Add frontend UI tests

Week 4 Plan:
- [ ] Finish off remaining front-end part from last week
- [ ] If frontend and backend part for MCQ weights are finished, then add necessary UI tests and make the PR ready for review.
- [ ] Calculate more statistics for MCQ questions to show in the results page
- [ ] Code review and fix

Week 5 Plan:
- [ ] Ensure that the CSV files include all data shown in the page for MCQ questions
- [ ] Update documentation for MCQ questions in the `InstructorHelp` page
- [ ] Implement the backend part of [MSQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/7281)
	- [ ] Update `QuestionDetails` class
	- [ ] Update `Logic` class
	- [ ] Update `Action` class
	- [ ] Add Corrosponding Unit and Integration tests
- [ ] Code review and fix

Week 6 Plan:
- [ ] Implement the frontend part of [MSQ questions: support attaching weights to options](https://github.com/TEAMMATES/teammates/issues/7281)
	- [ ] Update question template to add the new UI for MSQ weights
	- [ ] Add JS functionalities
	- [ ] Add necessary JS tests
	- [ ] Add frontend UI tests
- [ ] If frontend and backend part for MSQ weights are finished, then add necessary UI tests and make the PR ready for review.
- [ ] Update documentation for MSQ questions
- [ ] Code review and fix

Week 7 Plan:
- [ ] Calculate more statistics for MSQ questions (Total, average for each student) to show in the results page
- [ ] Ensure that the CSV files include all data shown in the page for MSQ questions
- [ ] Code review and fix

Week 8 Plan:
- [ ] Buffer time to finish off any remaining work from past weeks and for code review and fixes

Week 9 Plan:
- [ ] Implement the backend for [Rubric questions: allow weightages for sub questions](https://github.com/TEAMMATES/teammates/issues/7224)
	- [ ] Update `QuestionDetails` class
	- [ ] Update `Logic` class
	- [ ] Update `Action` class
	- [ ] Add Corrosponding Unit and Integration tests
- [ ] Code review and fix
- [ ] Implement the frontend for [Rubric questions: allow weightages for sub questions](https://github.com/TEAMMATES/teammates/issues/7224)
	- [ ] Update question template to add weights on each cell

Week 10 Plan:
- [ ] Implement the remaining frontend part of Rubric questions weights for each cell
	- [ ] Add JS functionalities
	- [ ] Add JS tests
	- [ ] Add Partial UI tests (Only the frontend part)
- [ ] If frontend and backend part are finished, then add necessary UI tests (with backend validations) and make the PR ready for review.
- [ ] Code review and fix

Week 11 Plan:
- [ ] Update documentation for Rubric question in the `InstructorHelp` page.
- [ ] Buffer week to finish off any remaining work from past weeks and for code review and fix

Week 12 Plan:
- [ ] Implement the backend part of the new question template
- [ ] Code review and fix

Week 13 Plan:
- [ ] Finish off any remaining work from last week
- [ ] Implement the frontend part of the new question template
- [ ] Update documentation
- [ ] Code review and fix

Week 14 Plan:
- [ ] Buffer time for review and iterations
