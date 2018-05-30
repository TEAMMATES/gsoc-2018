# Tan Heng Yeow

**Project: Spreadsheet Interface for Student Data UI** (non-GSoC project)

Overall Direction:
* Upgrade student data UI with spreadsheet interface. Interface should contain minimally columns `Section`, `Team`, `Name`, `Email`, `Comment`.
* Features to be implemented for the spreadsheet interface include (in decreasing priority):
    * Updating email field of student through a context menu.
    * Deleting selected students through tick boxes.
    * Merging cells with the same team together and auto merge students with same team together.
    * Scrolling and pagination.
    * Searching student entries.
* Pages that will be affected by the upgrade include:
    * `instructorCourseEnrollPage`: Current component replaced with the spreadsheet interface.
    * `instructorCourseDetailsPage`: Section below "Course Details" replaced with the spreadsheet interface.
    * `instructorStudentListPage`: Information inside each course's drop-downbox replaced with the spreadsheet interface.
* Update documentation and instructions for developers and users.
* Sufficient tests written for all new funtionalities.
* Ensure back-end validation works as intended as a result of the upgrade.
* Fix issues after integration tests, system tests and acceptance tests.

---

Week 1 Plan:
- [X] Finish up the remaining work for this [PR](https://github.com/TEAMMATES/teammates/pull/7568)
- [ ] Write tests for features in the spreadsheet interface

Works:
- 1st review ready at https://github.com/TEAMMATES/teammates/pull/8833#issuecomment-389790326
- Highlighted some thoughts on plan ahead at https://github.com/TEAMMATES/teammates/issues/8832#issuecomment-389788642

Retrospect on Week 1:

I have a better understanding of the Handsontable library and the APIs the library provides after working on the tasks this week. I have bookmarked the resources I searched for that aids me in implementing the spreadsheet interface during the process. I believe these resources will serve as a good reference from time to time when I work on new features for the spreadsheet interface at a later stage. 

Also, I highlighted some thoughts on how I envision the spreadsheet interface to be after working on the initial upgrade of the spreadsheet interface as I am more familiar with components of the spreadsheet interface now. I believe getting early feedback and advice on the plan ahead would prevent complications where the features might not fit in well with TEAMMATES or have potential conflicts with future plans.

I faced a problem getting a `Script error` after running javascript tests. I was stuck on this issue for about a few hours and it was blocking my progress of writing tests. Therefore, what I feel I did right was to highlight this issue to my mentors early while providing the actions I have attempted so that they can provide advice on how to get around it. Also, this serves as an update on the stage that I am currently at.

Week 2 Plan:
- [X] Complete tests for new features in the spreadsheet interface 
- [X] Update necessary documentation for developers and users
- [X] Fix issues after code review
- [ ] Deploy new spreadsheet interface

Works:
- 2nd review ready at https://github.com/TEAMMATES/teammates/pull/8833#issuecomment-391748250

Retrospect on Week 2:

I managed to solve problem faced last week and figured out a solution after my mentors gave me a nudge on a possibility that this issue is occuring. I felt that this process of trying to figure out a solution myself first before consulting for advice was beneficial in my learning progress. 

Also, I updated my mentors on the direction to adopt and the approach I am taking in advance so that they can give feedback on whether my approach is feasible. I believe this was necessary as the approach taken would affect how the new features should be implemented in later weeks.

I recapped and learnt useful `Array.prototype` methods through the code reviews provided, allowing me to write neater code. This knowledge will be useful for implementing the new features ahead. I also provided thoughts and clarified doubts in the code reviews, allowing me to put myself in my mentors' perspectivies and understand the rationale of their comments.

The work done this week involved improving code quality and testability. What I can improve on is to keep in mind the TDD approach to writing code, which was lacking in the previous week. This mindset would ensure that I do not spend as much effort and time refactoring the code I have written in multiple iterations. Also, I spent some time fixing lint issues after running `npm run lint` and `gradlew lint`. What I can do better is to test for lint issues after each new function/short logic is written so that I do not accumulate the lint issues. Also, through the common lint issues faced, I will take notes of them and write code that adheres to the coding standards, using linters only as a final form of verification.

Week 3 Plan:

Work on feature "Updating email field of an existing student through a context menu"

- [ ] Fix any new issues from Week 2
- [ ] Work on loading existing student data into `instructorCourseEnrollPage` through AJAX request
- [ ] Implement feature for context menu to allow highlighted `email` fields to be edited once after click
- [ ] Write tests for new feature above

Week 4 Plan:

Work on feature "Updating email field of student through a context menu"

- [ ] Finish up any remaining work from Week 3
- [ ] Implement dialog box to confirm changes
- [ ] Write tests for new feature above
- [ ] Integrate features into spreadsheet interface

Week 5 Plan:

Work on feature "Updating email field of student through a context menu"

- [ ] Finish up any remaining work from Week 4
- [ ] Update necessary documentation for developers and users for this feature
- [ ] Fix issues after code review
- [ ] Deploy new features for spreadsheet interface in production environment


Week 6 Plan:

Work on feature "Deleting selected students through tick boxes"

- [ ] Fix any new issues from Week 5
- [ ] Implement tick boxes as a column in spreadsheet interface
- [ ] Write tests for new feature above
- [ ] Implement functionality of delete button

Week 7 Plan:

Work on feature "Deleting selected students through tick boxes"

- [ ] Finish up any remaining work from Week 6
- [ ] Write tests for delete button
- [ ] Integrate features into spreadsheet interface
- [ ] Update necessary documentation for developers and users for this feature

Week 8 Plan:

Work on feature "Deleting selected students through tick boxes"

- [ ] Finish up any remaining work from Week 7 
- [ ] Fix issues after code review
- [ ] Deploy new features for spreadsheet interface in production environment

Week 9 Plan:

Work on feature "Merging cells with the same team together and auto merge students with same team together upon new entry"

- [ ] Fix any new issues from Week 8
- [ ] Implement functionality to merge cells with same team name together
- [ ] Write tests for new feature above
- [ ] Implement functionality to auto merge students with same team together upon new entry

Week 10 Plan:

Work on feature "Merging cells with the same team together and auto merge students with same team together upon new entry"

- [ ] Finish up any remaining work from Week 9 
- [ ] Write tests for new feature above
- [ ] Integrate features into spreadsheet interface
- [ ] Update necessary documentation for developers and users for this feature

Week 11 Plan:

Work on feature "Merging cells with the same team together and auto merge students with same team together upon new entry"

- [ ] Finish up any remaining work from Week 10
- [ ] Fix issues after code review
- [ ] Deploy new features for spreadsheet interface in production environment

Week 12 Plan:

Work on feature "Scrolling and pagination"

- [ ] Fix any new issues from Week 11
- [ ] Implement functionality to scroll across different pages
- [ ] Implement functionality to allow pagination across different pages
- [ ] Write tests for features above 
- [ ] Integrate features into spreadsheet interface
- [ ] Update necessary documentation for developers and users for this feature
- [ ] Fix issues after code review

Week 13 Plan:

Work on feature "Searching student entries"

- [ ] Finish up remaining work from Week 12 and deploy new feature for spreadsheet interface in production environment
- [ ] Implement search bar and search functionality to allow searching of student entries across different pages
- [ ] Write tests for new feature above
- [ ] Integrate features into spreadsheet interface
- [ ] Update necessary documentation for developers and users for this feature

Week 14 Plan:

Work on feature "Searching student entries"

- [ ] Finish up remaining work from Week 13
- [ ] Fix issues after code review
- [ ] Deploy new features for spreadsheet interface in production environment

