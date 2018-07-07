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
        * To allow edits on existing students' spreadsheet interface except the `Email` column. New column to be created for updates to existing student email.
    * 4th stage
        * To explore suitable feedback mechanism for each row in existing students' spreadsheet interface if edits to the field are not permitted after backend validation.
    * 5th stage
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
- 1st review ready [here](https://github.com/TEAMMATES/teammates/pull/8833#issuecomment-389790326)
- Highlighted some thoughts on plan ahead [here](https://github.com/TEAMMATES/teammates/issues/8832#issuecomment-389788642)

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
- 2nd review ready [here](https://github.com/TEAMMATES/teammates/pull/8833#issuecomment-391748250)

Retrospect on Week 2:

I managed to solve problem faced last week and figured out a solution after my mentors gave me a nudge on a possibility that this issue is occuring. I felt that this process of trying to figure out a solution myself first before consulting for advice was beneficial in my learning progress. 

Also, I updated my mentors on the direction to adopt and the approach I am taking in advance so that they can give feedback on whether my approach is feasible. I believe this was necessary as the approach taken would affect how the new features should be implemented in later weeks.

I recapped and learnt useful `Array.prototype` methods through the code reviews provided, allowing me to write neater code. This knowledge will be useful for implementing the new features ahead. I also provided thoughts and clarified doubts in the code reviews, allowing me to put myself in my mentors' perspectives and understand the rationale of their comments.

The work done this week involved improving code quality and testability. What I can improve on is to keep in mind the TDD approach to writing code, which was lacking in the previous week. This mindset would ensure that I do not spend as much effort and time refactoring the code I have written in multiple iterations. Also, I spent some time fixing lint issues after running `npm run lint` and `gradlew lint`. What I can do better is to test for lint issues after each new function/short logic is written so that I do not accumulate the lint issues. Also, through the common lint issues faced, I will take notes of them and write code that adheres to the coding standards, using linters only as a final form of verification.

Week 3 Plan:

2nd stage:
- [X] Fix any new issues from Week 2
- [X] Work on loading existing student data into `instructorCourseEnrollPage` through AJAX request
- [ ] Write tests for new feature above

Works:
- Updated this [PR](https://github.com/TEAMMATES/teammates/pull/8833) according to review comments. Commit shown [here](https://github.com/TEAMMATES/teammates/pull/8833/commits/6626c2c7d2b1698089556bc8d414277569bb2e26).
- Progress for this week marked at this [checkpoint]( https://github.com/TEAMMATES/teammates/pull/8884/commits/e620c8c598fce5b949fc8ad74659153099eeb7f9).

Retrospect on Week 3:

This week was fruitful for me as I became more familiar with parts of the codebase. The knowledge gained was beneficial in allowing me to start implementing the new proposed features as well writing better tests for them. 

I was able to identify how an `Action` is mapped from `ActionFactory`, which corresponds to the relevant `PageAction` file. Furthermore, I have a better understanding of the usage of `PageData` and `AppPage`, which provides utility methods to render specific page and a way to interact with a browser-loaded page respectively. In addition, this [tutorial](https://www.guru99.com/xpath-selenium.html) allowed me to understand more about XPath in Selenium WebDriver.

This knowledge allowed me to create a working AJAX back-end action to load existing student data into `instructorCourseEnrollPage`. Also, I was able pinpoint a specific WebElement using XPath, allowing me to write effective Selenium tests.

I believe the knowledge gained would serve as a good foundation for future back-end action(s) and Selenium tests needed for the new proposed features.

Week 4 Plan:

2nd stage:
- [X] Finish up any remaining work from Week 3
- [X] Add new separate spreadsheet interface in `instructorCourseEnrollPage` to show existing students. Loading of existing student data would be performed on this new spreadsheet interface. Ensure spreadsheet interface is read-only.
- [X] Include status box messages for existing students' spreadsheet interface:
    -  [X] Successfully loaded existing students
    - [X] No existing students (Hide existing students' spreadsheet interface in this case)
    - [X] Error loading existing student (include button to retry loading existing students)
- [ ] Write tests for new feature above

Works:
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8884/commits/2086fab545069a9397b6ba9fa373fee8985ee353).
- Fixed an existing [bug](https://github.com/TEAMMATES/teammates/pull/8881).

Retrospect on Week 4:

There was a major discussion on the end goal of the student data UI upgrade, which resulted in a shift of direction for the project. Part of the time was spent discussing the layout, exploring features for the upgrade and retuning the plan. I also spent time to study the existing implementation of `InstructorCourseEnrollSaveAction` and `instructorCourseStudentDetailsEditSaveAction`. Through the study, I fixed an existing bug related to how past session links are sent to new emails.

The study allowed me to be more familiar with how student details are updated on the back-end. It also gave me a chance to understand more about how the `Logic` Facade class and its child classes work. This process was beneficial for me as it gave me a better idea on how to proceed on to the next stage, which is to allow mass updates for existing students.

The shift in direction of the project also made me realized the importance of giving ample time for planned tasks of a project. Giving ample time allows flexibility and better adaptability of new plans on top of existing plans. Since this is an open-ended project, plans can change according to new inputs, thus a plan should provide room for flexibility. The previous plan had room for flexibility and I will maintain this behavior for future iterations.

Week 5 Plan:

3rd stage:
- [X] Fix any new issues from Week 4
- [X] Allow all existing columns in existing students' spreadsheet interface to be editable except the `Email` column.
- [X] Create a new column for users to update existing students' email in existing students' spreadsheet interface. 
- [ ] Create a new backend action to edit students fields in existing students' spreadsheet interface. 
    - [ ] Edits to `Section`, `Team`, `Name`, `Comments`
    - [ ] Edits to `Email` via values inserted in new column
- [ ] Write tests for new feature above

Works:
- Updated this [PR](https://github.com/TEAMMATES/teammates/pull/8884) according to review comments. Commit shown [here](https://github.com/TEAMMATES/teammates/pull/8884/commits/6b8c6daf7159df80a3711588f77bdbaa63ebfddf).
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8901/commits/70a5b9f0dbb0515f2b10dafb8bd6100eafb76471).

Retrospect on Week 5:

Part of this week's work involves referencing the behavior of how panels are expanded and collapsed in the existing system. This was done to address the concern of wasting computing cycles and UI space. This process allowed me to become more familiar with the JavaScript sections of the existing system. Also, it allowed me to gain first-hand experience on the issue of serving users at a large scale, where saving computing cycles is necessary to minimize or cut down unnecessary workload for the system.

I also spent some time to explore database related actions which involves `cascade` so that I have an idea on how the back-end interacts with the database. On top of the knowledge gained last week, I have a more complete idea on how updates are done end-to-end. This process gave me the confidence to create the new backend action to mass update students in the existing students' spreadsheet interface. 

Week 6 Plan:

3rd stage:
- [X] Finish up any remaining work from Week 5

Works:
- Fixed [regression](https://github.com/TEAMMATES/teammates/pull/8913)
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8901/commits/a5101e8300bcb66133afcb2e8b9ec415387a364b)

Retrospect on Week 6:

I managed to come up with a working version of the back-end action and front-end action to perform mass updates of students. As I was working through this, I realized that the next stage of work (explore suitable feedback mechanism for each row in existing students’ spreadsheet interface if edits to the field are not permitted after backend validation) would have complications with the existing behavior of expanding/collapsing panel of the existing students' data spreadsheet. The issue was that the current action of expanding the panel is mapped to a new AJAX action to fetch existing students data, thus there would be potential issues persisting state changes reflected from the back-end.

Upon discussion with my mentors, I was given some pointers and tips to ensure that the behavior is consistent throughout the system. This process reiterated the importance of working towards a targeted planned objective in a consistent manner. As this project's approach is to allow features to be made releaseable to users in stages, it is crucial that the features and behavior implemented builds on top of one another and they are in sync. Fortunately this issue was pointed out early (few weeks before the planned week for implementing the feedback mechanism). This would minimize chances where backtracking is needed due to negligence in the planning process. 

Week 7 Plan:

3rd stage:
- [ ] Fix any new issues from Week 6
- [ ] Create a new button to update changes to existing students' spreadsheet interface
- [ ] Design a modal box to display after the instructor clicks the new button to update changes to existing students' spreadsheet interface
    - [ ] Include option to resend past session links to potential new emails created
- [ ] Include status box messages to be shown in `instructorCourseEnroll` page after backend validation is performed for the updated changes.
- [ ] Write tests for new feature above

Week 8 Plan:

3rd stage:
- [ ] Finish up any remaining work from Week 7
- [ ] Complete tests for new feature above

Week 9 Plan:

4th stage:
- [ ] Fix any new issues from Week 8
- [ ] Implement skeleton feedback mechanism for each row in existing students' spreadsheet interface.

Week 10 Plan:

4th stage:
- [ ] Finish up any remaining work from Week 9
- [ ] Migrate status box messages to the new feedback mechanism.
- [ ] Write tests for new feature above

Week 11 Plan:

4th stage:
- [ ] Finish up any remaining work from Week 10
- [ ] Complete tests for new feature above

Week 12 Plan:

5th stage:
- [ ] Fix any new issues from Week 11
- [ ] Implement tick boxes as a column in spreadsheet interface

Week 13 Plan:

5th stage:
- [ ] Finish up any remaining work from Week 12
- [ ] Implement functionality of delete button
- [ ] Write tests for new feature above

Week 14 Plan:

5th stage:
- [ ] Finish up any remaining work from Week 13
- [ ] Complete tests for new feature above
