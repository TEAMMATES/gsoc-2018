# Sun Shengran

**Project: Recycle Bin**

Overall Direction:
- Build a recovery page for instructors to display user deleted courses, sessions and students
- Allow instructors to recover deleted courses, sessions and students from the recycle bin
- Allow instructors to permanently remove selected/all items from the recycle bin
- Build UI presentation for the deleted items and relevant functions
- Auto remove items from the recycle bin after a certain period
- Create comprehensive tests for the recovery feature

---

Week 1 Plan:
- [ ] Build UI frame/structure for displaying of deleted courses, sessions and students
- [ ] Create fake deleted items data for the acceptance testing of UI

Week 2 Plan:
- [ ] Add new attribute "deletedDate" for courses, sessions and students
- [ ] Modify relevant tests for courses, sessions and students

Week 3 Plan:
- [ ] Modify instructor delete items features by setting "deletedDate" without actually deleting the items
- [ ] Display only not deleted items ("deletedDate" is null) to users
- [ ] Modify relevant tests for instructors displaying & deleting of items

Week 4 Plan:
- [ ] Display the actual deleted items in the recovery page
- [ ] Add UI tests for the recovery page

Week 5 Plan:
- [ ] Add some documentation for current Recycle Bin feature in instructors help page
- [ ] Complete any work left from past weeks
- [ ] Buffer time for review and iterations

Week 6 Plan:
- [ ] Implement feature to allow users to delete selected items from recycle bin
- [ ] Implement feature to allow users to delete all courses/sessions/students from recycle bin
- [ ] Build UI presentation for deleting items

Week 7 Plan:
- [ ] Add tests for "Delete" & "Clear All" features
- [ ] Complete any work left from the last week

Week 8 Plan:
- [ ] Implement feature to allow users to restore selected courses (including corresponding sessions & students) from recycle bin
- [ ] Build UI presentation for restoring items
- [ ] Add tests for "Restore" of courses features

Week 9 Plan:
- [ ] Implement feature to allow users to restore selected sessions/students (if corresponding courses are not deleted) from recycle bin
- [ ] Build UI presentation for restoring items
- [ ] Add tests for "Restore" of sessions & students features

Week 10 Plan:
- [ ] Add some documentation for current Recycle Bin feature in instructors help page
- [ ] Complete any work left from past weeks
- [ ] Buffer time for review and iterations

Week 11 Plan:
- [ ] Implement auto-purging feature to check the deleted items and remove them once expired
- [ ] Trigger the event every time when user clicks on the recovery page
- [ ] Show message to user whether the recycle bin has been auto-updated, which items are expired and therefore permanently deleted

Week 12 Plan:
- [ ] Add tests for the auto-purging feature
- [ ] Complete any work left from the last week

Week 13 Plan:
- [ ] Add documentation for Recycle Bin feature in the instructors help page
- [ ] Complete any work left from past weeks

Week 14 Plan:
- [ ] Buffer time for review and iterations
