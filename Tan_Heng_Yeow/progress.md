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
- Understanding what have been implemented so far
- Fixing issues found manually
- Improving code quality and other concerns based on code review
- Experimenting with new UI/UX changes
- Faced `Script error` when writing QUnit tests

Week 2 Plan:
- [X] Complete tests for new features in the spreadsheet interface 
- [X] Update necessary documentation for developers and users
- [X] Fix issues after code review
- [ ] Deploy new spreadsheet interface

Works:
- 2nd review ready at https://github.com/TEAMMATES/teammates/pull/8833#issuecomment-391748250

Retrospect on Week 2:
- Fixed problem faced in Week 1. `Script error` was due to the `Handsontable` object not able to manipulate the existing DOM
- Refactored code to improve code quality and testability
- Experimenting with new UI/UX changes
- Set up staging server with latest changes
- Discussed and the plan ahead is to focus features on `instructorCourseEnrollPage` first. Migration can happen in other pages at a later stage.

Week 3 Plan:

Work on feature "Updating email field of an existing student through a context menu"

- [ ] Fix any new issues from Week 2
- [ ] Work on loading existing student data into `instructorCourseEnrollPage` through AJAX request
- [ ] Implement feature for context menu to allow highlighted `email` fields to be edited once after click
- [ ] Write tests for new feature above

Week 4 Plan:

Work on feature "Updating email field of student through a context menu"

- [ ] Finish up any remaining work from Week 3
- [ ] Fix issues after code review
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
- [ ] Fix issues after code review
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
- [ ] Fix issues after code review
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

