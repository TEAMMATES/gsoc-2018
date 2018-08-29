# Tan Heng Yeow

**Project: Spreadsheet Interface for Student Data UI** (non-GSoC project)

Overall Direction:
* Upgrade student data UI with spreadsheet interface. Interface should contain minimally columns `Section`, `Team`, `Name`, `Email`, `Comment`.
* Incremental stages for the upgrade process:
    * 1st stage
        * To replace current textbox in `instructorCourseEnrollPage` to a spreadsheet interface used for enrolling new students (new students' spreadsheet interface).
    * 2nd stage
        * To add a new separate spreadsheet interface in `instructorCourseEnrollPage` to show existing students (existing students' spreadsheet interface). This spreadsheet interface would be read-only. Both spreadsheet interfaces can be collapsed and expanded on demand. The existing students' spreadsheet interface would perform an AJAX action upon its first expansion to load existing students only if the spreadsheet interface is empty.
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
- Updated this [PR](https://github.com/TEAMMATES/teammates/pull/8833) according to review comments. Latest commit shown [here](https://github.com/TEAMMATES/teammates/pull/8833/commits/6626c2c7d2b1698089556bc8d414277569bb2e26).
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
- Updated this [PR](https://github.com/TEAMMATES/teammates/pull/8884) according to review comments. Latest commit shown [here](https://github.com/TEAMMATES/teammates/pull/8884/commits/6b8c6daf7159df80a3711588f77bdbaa63ebfddf).
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8901/commits/70a5b9f0dbb0515f2b10dafb8bd6100eafb76471).

Retrospect on Week 5:

Part of this week's work involves referencing the behavior of how panels are expanded and collapsed in the existing system. This was done to address the concern of wasting computing cycles and UI space. This process allowed me to become more familiar with the JavaScript sections of the existing system. Also, it allowed me to gain first-hand experience on the issue of serving users at a large scale, where saving computing cycles is necessary to minimize or cut down unnecessary workload for the system.

I also spent some time to explore database related actions which involves `cascade` so that I have an idea on how the back-end interacts with the database. On top of the knowledge gained last week, I have a more complete idea on how updates are done end-to-end. This process gave me the confidence to create the new backend action to mass update students in the existing students' spreadsheet interface. 

Week 6 Plan:

3rd stage:
- [X] Finish up any remaining work from Week 5

Works:
- Fixed [regression](https://github.com/TEAMMATES/teammates/pull/8913).
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8901/commits/a5101e8300bcb66133afcb2e8b9ec415387a364b).

Retrospect on Week 6:

I managed to come up with a working version of the back-end action and frontend action to perform mass updates of students. To cut down on computational resources, I stored a copy of the existing students' data when the data was first loaded into the spreadsheet. A separate function was written to only send updated student data to the back-end to update the students.

As I was working on this stage, I realized that the next stage of work (explore suitable feedback mechanism for each row in existing students’ spreadsheet interface if edits to the field are not permitted after backend validation) would have conflicts with the act of expanding/collapsing the panel of the existing students' data spreadsheet. This is because expanding the existing students' panel is mapped to a new AJAX action to fetch existing students data, thus there would be potential issues persisting state changes reflected from the back-end on the spreadsheet interface.

Upon discussion with my mentors, I was given some pointers and tips to ensure that the behavior is consistent throughout the system. This process reiterated the importance of working towards a targeted planned objective in a consistent manner. As this project's approach is to allow features to be made releaseable to users in stages, it is crucial that the features and behavior implemented builds on top of one another and they are in sync. Fortunately this issue was pointed out early (few weeks before the planned week for implementing the feedback mechanism). This would minimize chances where backtracking is needed due to negligence in the planning process. 

Week 7 Plan:

3rd stage:
- [X] Fix any new issues from Week 6
- [X] Create a new button to update changes to existing students' spreadsheet interface
- [ ] Design a modal box to display after the instructor clicks the new button to update changes to existing students' spreadsheet interface
    - [ ] Include option to resend past session links to potential new emails created
- [X] Include status box messages to be shown in `instructorCourseEnroll` page after backend validation is performed for the updated changes.
- [ ] Write tests for new feature above

Works:
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8901/commits/46290fb20c4b6ab3a175ec0d0936af081c17b895).
- Updated this [PR](https://github.com/TEAMMATES/teammates/pull/8884) according to review comments. Latest commit shown [here](https://github.com/TEAMMATES/teammates/pull/8884/commits/46290fb20c4b6ab3a175ec0d0936af081c17b895).

Retrospect on Week 7:

This week was spent updating this [PR](https://github.com/TEAMMATES/teammates/pull/8884) according to the review comments. After that, synchronization is done to match stage 3's [progress](https://github.com/TEAMMATES/teammates/pull/8901).

This week's work allowed me to learn more about the implementation of JavaScript promises (they represent the future result of an asynchronous operation) in TEAMMATES. There wasn't an existing implementation of JavaScript promises to reference in the codebase, thus it was an eye opener to me. It was also a good exposure for me as JavaScript promises are deemed the modern way to represent asynchronous operations compared to JavaScript callbacks.

In addition, this week's work also exposed me to writing tests for back-end AJAX actions. This experience allowed me to complete my knowledge of implementing AJAX related functionalities in TEAMMATES, from front-end, back-end to tests. The knowledge gained would be beneficial in aiding me to implement future end-to-end AJAX related actions in the codebase.

Upon working on stage 3 of the project, I realized that writing tests for the update action (which would update student details based on changes made to the existing students' spreadsheet interface) at this point is futile. This is because migration of the status box messages would be done in the next phase of the project, thus the potential tests written would be replaced and wasted. Therefore, I plan to combine the work done for stage 3 and 4 of the project together since they are intertwined, compared to the previous stages of the project which are independent of each other.

Week 8 Plan:

3rd stage:
- [X] Finish up any remaining work from Week 7
- [ ] Complete tests for new feature above

Works:
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8901/commits/aeebbcc6fe06b88bf123b50d6b394567f69b5b22).
- Updated this [PR](https://github.com/TEAMMATES/teammates/pull/8884) according to review comments. Latest commit shown [here](https://github.com/TEAMMATES/teammates/pull/8884/commits/cdbffba6654eddc65748af91f9df4903082ddc11).
- Fixed an existing [bug](https://github.com/TEAMMATES/teammates/pull/8936).

Retrospect on Week 8:

I managed to implement a modal box to confirm changes made to the existing students' spreadsheet interface. The modal box also provides an option to resend past session links to new emails if the user wants to change emails of existing students. The work involved both the front-end and back-end systems of the codebase and there was no major difficulty faced. Through the process of implementing the feature, I identified a bug in how the existing emails are generated and submitted a fix. 

Also, through this [PR](https://github.com/TEAMMATES/teammates/pull/8884), my mentor highlighted concerns with my commit practices. I have the tendency to make all required changes first and then commit changes by grouping related files together. This was done to minimize the potential chain of commits so that the reviewer would not have to see outdated commits and look through a huge list of commits. 

However, this practice can be improved as related changes might not always be grouped together properly through this practice. What I can do to improve is to follow a stricter commit organization requirements as specified by [here](https://oss-generic.github.io/process/) to the best of my ability.

Although the practice is not enforced in TEAMMATES, it would allow reviewers to have a better time reviewing the PR. Also it would be a good habit for me to adopt for future commits I will be making, regardless for the project or for other issues. Futhermore, following this practice would allow me to identify bad practices and advice others on how they can improve to make the lives of reviewers much easier. A smoother review would allow the progress of PRs to be made more efficient, which would benefit everyone.

As mentioned in last week's retrospect, I intend to combine the work done for stage 3 and 4 of the project together, thus tests will be written for the update action once the feedback mechanism is implemented.

Week 9 Plan:

4th stage:
- [X] Fix any new issues from Week 8
- [X] Implement skeleton feedback mechanism for each row in existing students' spreadsheet interface.

Works:
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8960/commits/055fd77d4b5ef7d736e0a1641f84c8f52f80f119).
- Worked on this [PR](https://github.com/TEAMMATES/teammates/pull/8954).

Retrospect on Week 9:

I took a short break from the existing project by working on other issues present in TEAMMATES. The reason was that I have been delving into mainly the `Courses` aspect of TEAMMATES and wanted to explore other aspects too. Furthermore, the [issue](https://github.com/TEAMMATES/teammates/issues/8791) was marked as `p.High` and was not actively worked on. By submitting the fix, I got a better understanding of AJAX implementation in TEAMMATES, the `Sessions` aspect and handling of `DateTime` fields. 

The rest of the week was spent exploring on a suitable mechanism for each row in the existing students' spreadsheet interface. The result of the research was that using renderers in `Handsontable` is suitable for the proposed feedback mechanism. This is because custom renderers can be built to suit the needs of this phase of the project by making use of the primitive renderers provided by `Handsontable`. For example, custom renderers allows us to display HTML content in a cell. I plan to use HTML status icons to indicate the type of feedback (success/failure) after backend validation and HTML tooltips as a way to display the content of the feedback. With the introduction of HTML content in the existing students' spreadsheet interface, there might be a risk of XSS attacks. To protect against XSS attacks, I took extra precaution to make sure that back-end sanitization has been put into place for the action I created in the previous stage that processes content sent from the existing students' spreadsheet interface.

I proceeded to implement a new column in the existing students' spreadsheet interface to show HTML green ticks as a form of experiment.

Week 10 Plan:

4th stage:
- [X] Finish up any remaining work from Week 9
- [X] Migrate status box messages to the new feedback mechanism.
- [ ] Write tests for new feature above

Works:
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8960/commits/d353ba96f328d497b958630464c124c04dd13b53).
- Worked on this [PR](https://github.com/TEAMMATES/teammates/pull/8976).

Retrospect on Week 10:

Prior to this stage of the project, I created a new back-end action to perform mass updates of students as mentioned in Week 6's retrospect. The action would result in a page refresh after updating students and show success/failure indicators in the form of status messages. As pointed out in the Week 6's retrospect, this behavior is not desirable. This is because a page refresh would cause the existing students' spreadsheet to be empty. When the spreadsheet is expanded again upon user click, an AJAX action would be executed to fetch the latest copy of existing students' data. This results in complications showing users any immediate feedback of the data sent after backend validation. Upon further discussion with my project mentors, feedback for success cases should be shown as well, not only error cases.

As such, the goal is to use an AJAX action to perform back-end validation of data and send the appropriate messages to the front-end. After which, the existing students' spreadsheet interface would be updated with the relevant feedback messages on the fly by modifying the DOM directly, without needing to refresh the page. 

I did this change in incremental steps. I first created a new AJAX action to process updated students and return success/failure indicators. After that, I modified both the front-end logic and the existing back-end action that performs mass update of students. As a result, the back-end action only does a page refresh upon a success indicator received from the front-end. In the final step, I replaced the back-end action completely with the current new AJAX action.

Moving on, I organized the error exception messages thrown and success messages in a way that it is suitable to be stored in the form of a Java `HashMap`. These data structures are sent to the frontend through AJAX and then stored as a JavaScript `Map`. Through this exercise, I recapped on Java `HashMap` and learnt tricks relevant to JavaScript `Map`. In addition, I used my knowledge of custom renderers learnt in the past two weeks to highlight the updated rows as a form of feedback using data stored in the JavaScript `Map`. Successful updated rows are highlighted in green and rows with errors are highlighted in red. Tooltips are available upon hover to aid the user in rectifying the error.

The final task for this week involved working on this [PR](https://github.com/TEAMMATES/teammates/pull/8976) due to a user request. I did research on pasting using `Handsontable` and proposed an update in the [issue](https://github.com/TEAMMATES/teammates/issues/8972) raised.

All in all, this week was fruitful as I did changes in incremental steps that were simple enough to prevent myself from getting overwhelmed with tasks. I am now more well versed with creating and modifying existing actions to perform AJAX requests and also do a page refresh if necessary. Furthermore, I believe my increased familiarity with handling Java `HashMap` and JavaScript `Map` is useful in completing the work for this phase of the project as they serve as the backbone in providing feedback from the back-end to the front-end.

Week 11 Plan:

4th stage:
- [X] Finish up any remaining work from Week 10
- [ ] Complete tests for new feature above

Works:
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/8989#issuecomment-408049261).
- Fix and merged this [PR](https://github.com/TEAMMATES/teammates/pull/8976).
- Worked on and merged this [PR](https://github.com/TEAMMATES/teammates/pull/8996).
- Updated this [PR](https://github.com/TEAMMATES/teammates/pull/8884) according to review comments. Latest commit shown [here](https://github.com/TEAMMATES/teammates/pull/8884/commits/a0349305ad6c23f352f8d6c20ba10ae22d8869bf).

Retrospect on Week 11:

This week's work involves improving the status message shown during the enroll process to be consistent with stage 3 and 4 of the proposed features. There were no major difficulties faced as I have done similar type of work in the last week. I submitted an early PR and obtained some feedback for improvement before implementing tests.

In order to minimize huge changes to the existing codebase, I submitted work that followed this [approach](https://github.com/TEAMMATES/teammates/pull/8989#issuecomment-408110265). After some discussion, we reached a consensus to remove the existing enrollment result page and use AJAX only to display success/error messages. I felt what I did right was to obtain early feedback on production code before writing test code. This is because time would be wasted if I wrote test code only to find out that the production code could be better written using a different approach.

Week 12 Plan:

5th stage:
- [X] Fix any new issues from Week 11
- [X] Implement check boxes as a column in spreadsheet interface

Works:
- Progress for this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/9019/commits/d0a544e843751ff0bbd1ef82b7dae215cc49f8dd).
- Worked on this [PR](https://github.com/TEAMMATES/teammates/pull/9017).
- Updated this [PR](https://github.com/TEAMMATES/teammates/pull/8884) according to review comments. Latest commit shown [here](https://github.com/TEAMMATES/teammates/pull/8884#issuecomment-409219892).

Retrospect on Week 12:

This week's work includes working on the new approach to improve the status message shown during the enroll process. There were no major difficulties faced and the lessons learnt from past work and code reviews aided me a lot in the implementation.

Also, I managed to implement a column of check boxes in the spreadsheet interface. Initially, I wanted to design a check box to be placed in the column header. When the checkbox in the header is clicked, all the student rows will be selected/unselected. However, I realized that there would be potential complications if I approach it this way. As the check box is in HTML, it would cause inconsistencies in rendering the section headers as they would be parsed both in the front-end and back-end. As a result, I changed the section header to be an empty string and implemented buttons to select/unselect all student rows instead.

Week 13 Plan:

5th stage:
- [X] Finish up any remaining work from Week 12
- [X] Implement functionality of delete button
- [ ] Write tests for new feature above

Works:
- Progress of this week marked at this [checkpoint](https://github.com/TEAMMATES/teammates/pull/9019/commits/245127a30d6fbcebcab6b50f7dbb89fa1741bb14).
- Discussion made for this [PR](https://github.com/TEAMMATES/teammates/pull/9017).

Retrospect on Week 13:

I managed to complete the final phase of the proposed project, which includes setting up a delete action to delete selected students from the existing students' spreadsheet interface. The work includes dealing with the full stack and there were no major difficulties faced due to my increased familiarity with the `Courses` aspect.

The rest of the week was spent discussing on better design choices to improve the status messages for enrollment based on the progress made. The discussion included better back-end class design choices and setting up suitable API endpoints. The discussion was fruitful and necessary as it would affect how status messages will be shown in the existing students' spreadsheet interface after updating student entries. This is because their end behavior would be very similar, which involves highlighting the specific student entry row to indicate its current status (success/failure).

Week 14 Plan:

5th stage:
- [X] Finish up any remaining work from Week 13
- [ ] Complete tests for new feature above

Works:
- Discussion made for this [PR](https://github.com/TEAMMATES/teammates/pull/9017).

Retrospect on Week 14:

This week was spent on further in-depth discussion on the optimal direction ahead to improve the status message after enrollment. The discussion was necessary because of a few reasons:
1. No functionalities in TEAMMATES uses AJAX response data to modify the DOM extensively yet, so there's no standard to take reference from. This means that a thorough design has to be decided from scratch.
2. Modifications would be made to existing codebase because the enrollment result page would not be used anymore. 
3. Existing feedback that was previously present in the enrollment result page has to be migrated to be shown in the enroll page in a suitable format. 
4. Old tests would be deleted and new tests would be added according to the new design.
5. It would affect the design implementation of status messages shown for the update feature discussed last week.

The discussion went well and there was substantial groundwork made for the design choices to proceed with implementation. Moving forward, I will spend my free time to implement the remaining tasks based on any new discussion made for the proposed student data user interface upgrade.
