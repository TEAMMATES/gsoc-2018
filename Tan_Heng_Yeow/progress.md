# Tan Heng Yeow

**Project: Spreadsheet Interface for Student Data UI** (non-GSoC project)

Overall Direction:
* Upgrade student data UI with spreadsheet interface. Interface should contain minimally columns `Section`, `Team`, `Name`, `Email`, `Comment`.
* Incremental stages for the upgrade process:
    * 1st stage
        * To replace current textbox in `instructorCourseEnrollPage` to a spreadsheet interface used for enrolling new students (new students' spreadsheet interface).
    * 2nd stage
        * To add a new separate spreadsheet interface in `instructorCourseEnrollPage` to show existing students (existing students' spreadsheet interface). This spreadsheet interface would be read-only.
    * 3rd stage
        * To add existing buttons from `instructorCourseDetailsPage` into existing students' spreadsheet interface.
    * 4th stage
        * To allow edits on existing students' spreadsheet interface except the `Email` column. New column to be created for updates to existing student email.
    * 5th stage
        * To explore suitable feedback mechanism for each row in existing students' spreadsheet interface if edits to the field are not permitted after backend validation.
    * 6th stage
        * To add a column or way to allow deleting selected students in existing students' spreadsheet interface.

* Pages that will be affected by the upgrade include:
    * Relevant now:
        * `instructorCourseEnrollPage`: Current component replaced with the spreadsheet interface.
    * To consider in the future:
        * `instructorCourseDetailsPage`: Section below "Course Details" replaced with the spreadsheet interface.
        * `instructorStudentListPage`: Information inside each course's drop-downbox replaced with the spreadsheet interface.
* Update documentation and instructions for developers and users.
* Sufficient tests written for all new funtionalities.
* Ensure back-end validation works as intended as a result of the upgrade.
* Fix issues after integration tests, system tests and acceptance tests.

---

Week 1 Plan:

1st stage:
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

1st stage:
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

2nd stage:
- [ ] Fix any new issues from Week 2
- [ ] Work on loading existing student data into `instructorCourseEnrollPage` through AJAX request
- [ ] Write tests for new feature above

Week 4 Plan:

2nd stage:
- [ ] Finish up any remaining work from Week 3
- [ ] Add new separate spreadsheet interface in `instructorCourseEnrollPage` to show existing students. Loading of existing student data would be performed on this new spreadsheet interface. Ensure spreadsheet interface is read-only.
- [ ] Include status box messages for existing students' spreadsheet interface:
    -  [ ] Successfully loaded existing students
    - [ ] No existing students (Hide existing students' spreadsheet interface in this case)
    - [ ] Error loading existing student (include button to retry loading existing students)
- [ ] Write tests for new feature above

Week 5 Plan:

3rd stage:
- [ ] Fix any new issues from Week 4
- [ ] Add existing buttons from `instructorCourseDetailsPage` into existing students' spreadsheet interface. These buttons include:
    - [ ] View
    - [ ] Edit
    - [ ] Send Invite
    - [ ] Delete
    - [ ] All Records
    - [ ] Delete All Students
- [ ] Add code to backend functionality of the buttons to redirect back to `instructorCourseEnroll` if necessary
- [ ] Add code to backend functionality of the buttons to show status messages in `instructorCourseEnroll` if necessary
- [ ] Write tests for new feature above

Week 6 Plan:

3rd stage:
- [ ] Finish up any remaining work from Week 5
- [ ] Complete tests for new feature above

Week 7 Plan:

4th stage:
- [ ] Fix any new issues from Week 6
- [ ] Allow all existing columns in existing students' spreadsheet interface to be editable except the `Email` column.
- [ ] Create a new column for users to update existing students' email in existing students' spreadsheet interface. 
- [ ] Create a new backend action to edit students fields in existing students' spreadsheet interface. 
    - [ ] Edits to `Section`, `Team`, `Name`, `Comments`
    - [ ] Edits to `Email` via values inserted in new column
- [ ] Write tests for new feature above

Week 8 Plan:

4th stage:
- [ ] Finish up any remaining work from Week 7

Week 9 Plan:

4th stage:
- [ ] Fix any new issues from Week 8
- [ ] Create a new button to update changes to existing students' spreadsheet interface
- [ ] Design a model box to show after the instructor clicks the new button to update changes to existing students' spreadsheet interface
    - [ ] Include option to resend past session links to potential new emails created
- [ ] Include status box messages to be shown in `instructorCourseEnroll` page after backend validation is performed for the updated changes.
- [ ] Write tests for new feature above

Week 10 Plan:

4th stage:
- [ ] Finish up any remaining work from Week 9
- [ ] Complete tests for new feature above

Week 11 Plan:

5th stage:
- [ ] Implement skeleton feedback mechanism for each row in existing students' spreadsheet interface.
- [ ] Migrate status box messages to the new feedback mechanism.
- [ ] Write tests for new feature above

Week 12 Plan:

5th stage:
- [ ] Finish up any remaining work from Week 11
- [ ] Complete tests for new feature above

Week 13 Plan:

6th stage
- [ ] Fix any new issues from Week 12
- [ ] Implement tick boxes as a column in spreadsheet interface
- [ ] Write tests for new feature above
- [ ] Implement functionality of delete button

Week 14 Plan:

6th stage
- [ ] Finish up any remaining work from Week 13
- [ ] Complete tests for new feature above
