# Sun Shengran

**Project: Recycle Bin**

Overall Direction:
- Build a recovery page for instructors to display user deleted courses and sessions (whose corresponding courses are not deleted)
- Allow instructors to recover selected/all courses and sessions from the recycle bin
- Allow instructors to permanently remove selected/all items from the recycle bin
- Build UI presentation for the deleted items and relevant functions
- Auto remove items from the recycle bin after a certain period
- Create comprehensive tests for the recovery feature

---

Week 1 Plan:
- [x] Build UI frame/structure for displaying of deleted courses and sessions
- [x] Create fake deleted items data for the acceptance testing of UI

Week 1 Work:

- [x] Created PR #8835 [Instructor: recycle bin feature: add instructor recovery page mock up #8834](https://github.com/TEAMMATES/teammates/pull/8835)

Week 1 Retrospect:

This week I built an instructor recovery page and created some fake courses/sessions data for UI testing before the actual development. Since I was new to JSP, it took me some time to figure out how to create a new page and navigate to it by clicking the label on nav bar.

Week 2 Plan:
- [x] Add new attribute "deletedDate" for courses and sessions
- [x] Modify relevant tests for courses and sessions

Week 2 Work:

- NA

Week 2 Retrospect:

This week I created a new attribute "deletedAt" in storage for "Courses", and set the value of "deletedAt" every time user deleted a course instead of actually deleting it. I also managed to create a Recycle Bin table layout for deleted courses in instructor recovery page. The major difficulty I faced this week is that the new attribute I created cannot be updated, thus the courses deleted by user cannot be shown in Recycle Bin. But later I found out that instead of actually updating the attributes in course, "updateCourse" method creates a new course and adds this course directly to the datastore.

Week 3 Plan:
- [x] Modify instructor delete items features by setting "deletedDate" without actually deleting the items
- [x] Display only not deleted items ("deletedDate" is null) to users
- [x] Modify relevant tests for instructors displaying & deleting of items

Week 3 Work:

- [x] Created PR #8853 [Instructor: recycle bin feature: allow restore and delete courses in recovery page #8852](https://github.com/TEAMMATES/teammates/pull/8853)

Week 3 Retrospect:

This week I deleted instructor recovery page and moved the Recycle Bin for courses to instructor courses page due to Prof's suggestion. Also, I implemented actions for restoring & permanently deleting a single course. No major difficulties encountered.

Week 4 Plan:
- [x] Display the actual deleted items in the recovery page
- [ ] Add UI tests for the recovery page

Week 4 Work:

- [x] Committed to PR #8853 [Instructor: recycle bin feature: allow restore and delete courses in recovery page #8852](https://github.com/TEAMMATES/teammates/pull/8853)

Week 4 Retrospect:

This week I implemented actions for restoring & permanently deleting all courses in Recycle Bin. The major difficulty I faced this week is making a panel for deleted courses table. Since I wasn't quite familiar with JavaScript, I was not able to control the icon and buttons on the panel heading. By this time, the whole feature of Recycle Bin for courses is done.

Week 5 Plan:
- [x] Add some documentation for current Recycle Bin feature in instructors help page
- [x] Complete any work left from past weeks
- [x] Buffer time for review and iterations

Week 5 Work:

- [x] Committed to PR #8853 [Instructor: recycle bin feature: allow restore and delete courses in recovery page #8852](https://github.com/TEAMMATES/teammates/pull/8853)

Week 5 Retrospect:

This week I created a new attribute "deletedTime" in storage for "Feedback Sessions" and set the value every time user deleted a session instead of actually deleting it. I also managed to create a Recycle Bin table layout for deleted feedback sessions in instructor feedback sessions page. No major difficulties encountered.

Week 6 Plan:
- [x] Implement feature to allow users to delete selected items from recycle bin
- [x] Implement feature to allow users to delete all courses/sessions from recycle bin
- [x] Build UI presentation for deleting items

Week 6 Work:

- [x] Created PR #8907 [Instructor: recycle bin feature: allow restore and delete sessions in instructor feedback sessions page #8906](https://github.com/TEAMMATES/teammates/pull/8907)

Week 6 Retrospect:

This week I implemented actions for restoring & permanently deleting single/all feedback sessions in Recycle Bin. By this time, the whole feature of Recycle Bin for feedback sessions is done. No major difficulties encountered. Waiting for review.

Week 7 Plan:
- [ ] Add tests for "Delete Permanently" & "Delete All Courses/Sessions" features
- [x] Complete any work left from the last week

Week 7 Work:

- [x] Committed to PR #8907 [Instructor: recycle bin feature: allow restore and delete sessions in instructor feedback sessions page #8906](https://github.com/TEAMMATES/teammates/pull/8907)
- [x] Committed to PR #8853 [Instructor: recycle bin feature: allow restore and delete courses in recovery page #8852](https://github.com/TEAMMATES/teammates/pull/8853)

Week 7 Retrospect:

This week I managed to add a panel for both deleted courses and deleted feedback sessions. I moved action buttons for all courses/sessions to the panel heading, similar to instructor home page & student list page to avoid confusion. No major difficulties encountered. Waiting for review.

Week 8 Plan:
- [x] Implement feature to allow users to restore selected/all courses (including corresponding sessions & students) from recycle bin
- [x] Build UI presentation for restoring items
- [ ] Add tests for "Restore" & "Restore All Courses" of courses features

Week 8 Work:

- [x] Created PR #8928 [Instructor: recycle bin feature: add instructions for managing deleted courses in instructor help page #8927](https://github.com/TEAMMATES/teammates/pull/8928)

Week 8 Retrospect:

This week I added instructions in instructor help page on the management (i.e. viewing deleted courses, restoring courses, permanently deleting courses) of Recycle Bin for courses. No major difficulties encountered. Waiting for review.

Week 9 Plan:
- [x] Implement feature to allow users to restore selected/all sessions and student responses (if corresponding courses are not deleted) from recycle bin
- [x] Build UI presentation for restoring items
- [ ] Add tests for "Restore" & "Restore All Sessions" of sessions features

Week 9 Work:

- [x] Created PR #8953 [Instructor: recycle bin feature: add tests for deleting & restoring of courses #8952](https://github.com/TEAMMATES/teammates/pull/8953)
- [x] Merged PR #8853 [Instructor: recycle bin feature: allow restore and delete courses in recovery page #8852](https://github.com/TEAMMATES/teammates/pull/8853)
- [x] Committed to PR #8907 [Instructor: recycle bin feature: allow restore and delete sessions in instructor feedback sessions page #8906](https://github.com/TEAMMATES/teammates/pull/8907)

Week 9 Retrospect:

This week I have written tests for Recycle Bin feature in Instructor Courses Page. During the process I found some issues & bugs on access control. Thus, I modified the methods for checking instructor privileges in action files (i.e. `InstructorCourseRestoreAllRecoveryCoursesAction.java`). I also managed to disable delete/restore (all) buttons if instructor does not have the corresponding privilege. No major difficulties encountered.

Week 10 Plan:
- [x] Add some documentation for current Recycle Bin feature in instructors help page
- [x] Complete any work left from past weeks
- [x] Buffer time for review and iterations

Week 10 Work:

- [x] Created PR #8965 [Instructor: recycle bin feature: add instructions for managing deleted sessions in instructor help page #8964](https://github.com/TEAMMATES/teammates/pull/8965)
- [x] Created PR #8969 [Instructor: recycle bin feature: add tests for deleting & restoring of sessions #8968](https://github.com/TEAMMATES/teammates/pull/8969)
- [x] Merged PR #8967 [Instructor Home Page: Hide options for instructors without corresponding privileges #8962](https://github.com/TEAMMATES/teammates/pull/8967)
- [x] Merged PR #8973 [InstructorHomePageUiTest & InstructorCoursesPageUiTest failing on 'recycling-bin' branch #8971](https://github.com/TEAMMATES/teammates/pull/8973)
- [x] Merged PR #8975 [InstructorHomePageUiTest & InstructorCoursesPageUiTest failing due to rebase errors #8971](https://github.com/TEAMMATES/teammates/pull/8975)

Week 10 Retrospect:

This week I added instructions in instructor help page on the management (i.e. viewing deleted sessions, restoring deleted sessions, permanently deleting sessions) of Recycle Bin for feedback sessions. I have also finished adding tests for Recycle Bin feature in Instructor Feedback Sessions Page. Some tests failed (on `recycling-bin` branch) on Travis CI & Appveyor this week, but I've managed to fix them. No major difficulties encountered.

Week 11 Plan:
- [ ] Implement auto-purging feature to check the deleted items and remove them once expired
- [ ] Trigger the event every time when user clicks on the recovery page
- [ ] Show message to user whether the recycle bin has been auto-updated, which items are expired and therefore permanently deleted

Week 11 Work:

- [x] Merged PR #8928 [Instructor: recycle bin feature: add instructions for managing deleted courses in instructor help page #8927](https://github.com/TEAMMATES/teammates/pull/8928)
- [x] Committed to PR #8907 [Instructor: recycle bin feature: allow restore and delete sessions in instructor feedback sessions page #8906](https://github.com/TEAMMATES/teammates/pull/8907)
- [x] Committed to PR #8953 [Instructor: recycle bin feature: add tests for deleting & restoring of courses #8952](https://github.com/TEAMMATES/teammates/pull/8953)

Week 11 Retrospect:

This week I've been focusing on fixing issues in my PRs due to mentors' comments. No major difficulties encountered.

Week 12 Plan:
- [ ] Add tests for the auto-purging feature
- [x] Complete any work left from the last week

Week 12 Work:

- [x] Merged PR #8953 [Instructor: recycle bin feature: add tests for deleting & restoring of courses #8952](https://github.com/TEAMMATES/teammates/pull/8953)
- [x] Merged PR #9005 [Instructor: Courses Page: Recycle Bin feature for courses #9002](https://github.com/TEAMMATES/teammates/pull/9005)
- [x] Merged PR #8907 [Instructor: recycle bin feature: allow restore and delete sessions in instructor feedback sessions page #8906](https://github.com/TEAMMATES/teammates/pull/8907)
- [x] Merged PR #8965 [Instructor: recycle bin feature: add instructions for managing deleted sessions in instructor help page #8964](https://github.com/TEAMMATES/teammates/pull/8965)
- [x] Created PR #9014 [Instructor: recycle bin feature: refactor term 'recovery' to other meaningful terms #9013](https://github.com/TEAMMATES/teammates/pull/9014)

Week 12 Retrospect:

This week the Recycle Bin feature for courses has been successfully merged to master. Due to massive commits and high dependency among my PRs, I have learned to rebase my branches instead of simply merging branches. This week I mainly focused on refactoring of term 'recovery' to some other meaningful terms. No major difficulties encountered.

Week 13 Plan:
- [x] Add documentation for Recycle Bin feature in the instructors help page
- [ ] Complete any work left from past weeks

Week 13 Work:

- [x] Committed to PR #9014 [Instructor: recycle bin feature: refactor term 'recovery' to other meaningful terms #9013](https://github.com/TEAMMATES/teammates/pull/9014)
- [x] Created PR #9039 [Instructor: delete all courses permanently: specify courses being deleted #9038](https://github.com/TEAMMATES/teammates/pull/9039)

Week 13 Retrospect:

This week I focused on modifying the confirmation dialog for deleting all courses in Recycle Bin. No major difficulties encountered. Waiting for final review.

Week 14 Plan:
- [x] Buffer time for review and iterations

Week 14 Work:

- [x] Merged PR #8969 [Instructor: recycle bin feature: add tests for deleting & restoring of sessions #8968](https://github.com/TEAMMATES/teammates/pull/8969)
- [x] Merged PR #9014 [Instructor: recycle bin feature: refactor term 'recovery' to other meaningful terms #9013](https://github.com/TEAMMATES/teammates/pull/9014)
- [x] Committed to PR #9039 [Instructor: delete all courses permanently: specify courses being deleted #9038](https://github.com/TEAMMATES/teammates/pull/9039)
- [x] Merged PR #9049 [Instructor: Feedback Sessions Page: Recycle Bin feature for sessions #9048](https://github.com/TEAMMATES/teammates/pull/9049)

Week 14 Retrospect:

This week the Recycle Bin feature for feedback sessions has been successfully merged into `recycling-bin` branch, and I have created a PR to merge it into `master`. I also refactored the confusing term `recovery` to other meaningful terms (i.e. `soft-deleted`, `RecycleBin`). No major difficulties encountered.
