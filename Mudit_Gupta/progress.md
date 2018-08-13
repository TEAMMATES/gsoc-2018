# Mudit Gupta

**Project: Usability Hero**

Overall Direction:
- Provide Context specific help
- Improve Getting Started guide
- Improve documentation structure
- Resolve UI/UX issues

---

Week 1 Plan:
- [x] Work on [Student: feedback submission: distribution points question: explain if equal points are not allowed](https://github.com/TEAMMATES/teammates/issues/8817)
- [x] Discuss with Cara further work to be done on Getting started guide and help docs

Week 1 Work:
- [x] Initial aim of the issue [Student: feedback submission: distribution points question: explain if equal points are not allowed](https://github.com/TEAMMATES/teammates/issues/8817) was to simply add explanation but the issue was further extended to add enhancements to warnings to ditribute points style questions

Week 1 Retrospect:
For the first week, I spent a lot of time just understanding the code and design of teammates in general. Reading [design docs](https://github.com/TEAMMATES/teammates/blob/master/docs/design.md) repeatedly was very helpful. Also learnt more about JSP and servlets. Constantly I had some detailed discussions on the need and viability of different features in my proposal. As discussed with Prof Damith it was best to focus on enhancing current UI elements instead of building new features from scratch. The plan of incorporating a sidebar for intstructor docs was scrapped in the end as it was deemed unnecessary.

Week 2 Plan:
- [x] Front end development for sidebar of instructor help (scrapped)
- [x] UI Enhancements for Distribute points style questions
- [x] Write browser tests for enhancements

Week 2 work:
- [x] Worked on [Enhancements to distribute points questions](https://github.com/TEAMMATES/teammates/pull/8836) as an extension of issue [8817](https://github.com/TEAMMATES/teammates/issues/8817). Finished work on the initial version. Constant iterations to try out different designs.
- [x] Added tests for [Enhancements to distribute points questions](https://github.com/TEAMMATES/teammates/pull/8836)
- [x] Approved: [Instructor: creating a session: able to manipulate the option when checkbox is not checked](https://github.com/TEAMMATES/teammates/pull/8846)

Week 2 retrospect:
There was some confusion regarding the existing implementation (from PR [8577](https://github.com/TEAMMATES/teammates/pull/8577)) of warnings displayed in distribute points questions due to which refactoring was done for the new version to ensure backward compatibility.

Week 3 Plan:
- [x] Solve UX issues on the side
- [x] Simplify views for complicated tasks by hiding details/advanced options

Week 3 work:
  - [x] Created several mockups for simplifying different UI elements and pages. 
  - Improving filtering interface on Students page
  - Eliminating action buttons for each row in tables by building a row selection mechanism
  - Proposed changes to constraints displayed for rank style questions to follow the same pattern as distribute points questions
  - Using a slider to select min/max number of recipients in rank style questions
  - [x] Approved: [Student: feedback submission: distribution points question: explain if equal points are not allowed](https://github.com/TEAMMATES/teammates/pull/8836)
- [x] Worked on [Instructor: Add Course title to Student Details page](https://github.com/TEAMMATES/teammates/pull/8861) and implemented some further enhancements
- [x] Halfway done with [Student: Feedback submission: Rank question: Improve explanation regarding ranking constraints](https://github.com/TEAMMATES/teammates/pull/8870). [8836](https://github.com/TEAMMATES/teammates/pull/8836) needs to be merged before this one can be finished due to dependencies

Week 3 retrospect:
By this week I realized that a lot of time is spent refactoring just because of conflict in design decisions so I decided to make use of mockups even for simple changes to make sure everyone is on the same page before I begin coding.

Week 4 Plan:
- [x] Finding remaining views that need simplification and fixing those
- [x] Write tests for new views

Week 4 work:
- [x] Worked on [Student: submit responses: use a more friendly way to choose evaluee](https://github.com/TEAMMATES/teammates/pull/8878) to augment evaluee options with team and section information. Additionally implemented a sorting feature to sort evaluees based on team and section information 
- [x] Worked on [Instructor: edit MCQ question: give an easier way to reorder options](https://github.com/TEAMMATES/teammates/pull/8889) to implement a drag and drop feature to reorder options

Week 4 retrospect:
Created 2 PRs this week for different enhancements while fixing issues with past PRs. Also had a detailed discussion with Cara and rest of mentors regarding Interactive tutorial and enhancing Cara's Instructor help docs. The conclusion in a nutshell was that interactive tutorial wasn't need of the hour since its use is to generally introduce novice users to basic features. Prof Damith suggested that it would instead be more profitable to focus on a small group of competent and loyal users who need guidance with advanced features. Regarding the instructor documentation, I made a suggestion to extend Cara's version to provide guidance on advanced options but this is still under discussion. 

Week 5 Plan:
- [x] Buffer period to resolve pending work from week 1-4
- [x] Fix issues after code review

Week 5 work:
- [x] Added tests for following PRs:
  - [Instructor: Add Course title to Student Details page](https://github.com/TEAMMATES/teammates/pull/8861)
  - [Student: submit responses: use a more friendly way to choose evaluee](Student: submit responses: use a more friendly way to choose evaluee)
  - [Instructor: edit MCQ question: give an easier way to reorder options](https://github.com/TEAMMATES/teammates/pull/8889)
- [x] Fixed remaining issues. All PRs ready for review.

Week 5 retrospect:
I had initally planned on finishing tests by week 4 for all enhancements so far but due to debugging issues, adding tests was mostly done in this week. Adding tests for MCQ questions reorder options took a while. Simulating drag and drop behaviour was tricky since the widget being used requires the option to be dragged slowly to the target location for the grid to shift. Selenium's drag and drop API is instantaneous which doesn't change the grid structure at all and the test fails. I tried emulating a slow drag movement by doing multiple small movements to target instead of one single instantaneous movement.

Week 6 Plan:
- [ ] ~~Mockups for enhancements to Getting started guide~~ (scrapped)
- [ ] ~~Develop use cases/user stories + UI workflows for enhancements to Getting started guide~~ (scrapped)
- [x] In depth discussion to ensure common ground on design
- [x] Mockups for enhancements to Feedback session creation
- [x] Implement drag and drop feature for other question types

Week 6 work:
- [x] Created mockups for improvements to feedback session creation and managing advanced settings. Key ideas involved:
- Progressive disclosure
- Marking mandatory fields
- Improving display of more information of advanced settings
- Improving wording of text
- [x] Merged: [Student: feedback submission: distribution points question: explain if equal points are not allowed](https://github.com/TEAMMATES/teammates/pull/8836)
- [x] Merged: [Instructor: creating a session: able to manipulate the option when checkbox is not checked](https://github.com/TEAMMATES/teammates/pull/8846)
- [x] Implemented drag and drop feature for MSQ questions. Extended [Instructor: edit MCQ question: give an easier way to reorder options](https://github.com/TEAMMATES/teammates/pull/8889) to include MSQ questions.
- [x] Implemented drag and drop feature for Distribute points questions [Instructor: Edit distribute points question: reorder options using drag and drop](https://github.com/TEAMMATES/teammates/pull/8916)
- [x] Implemented drag and drop feature for Rank questions. Extended [Instructor: Edit distribute points question: reorder options using drag and drop](https://github.com/TEAMMATES/teammates/pull/8916) to include Rank questions.


Week 6 Retrospect:
Based on the discussion that took place in week 4 and 5 with Prof Damith and my mentors, we decided to focus on making advanced features easier to use. So the initial plan to work on Getting started guide was scrapped and I researched into current bottlenecks while setting advanced options. I drew some mockups to improve the same as shown above. Some of these issues were addressed in later PRs. We decided to extend drag and drop functionality to other question types as well. In this week I also had to spend some time resolving merge conflicts for drag and drop PR due to previous enhancements made to distribute points questions.

Week 7 Plan:
- [ ] ~~Front end development for enhancements to Getting started guide~~ (scrapped)
- [x] Writing Selenium tests
- [x] Finish work on [Student: Feedback submission: Rank question: Improve explanation regarding ranking constraints](https://github.com/TEAMMATES/teammates/pull/8870)

Week 7 Work:
- [x] Review ready PR: [Instructor: edit MCQ question: give an easier way to reorder options](https://github.com/TEAMMATES/teammates/pull/8889) after adding tests for MSQ questions.
- [x] Review ready PR: [Instructor: Edit distribute points question: reorder options using drag and drop](https://github.com/TEAMMATES/teammates/pull/8916) after adding tests for rank and distribute points questions.
- [x] Review ready PR: [Student: Feedback submission: Rank question: Improve explanation regarding ranking constraints](https://github.com/TEAMMATES/teammates/pull/8870) after adding tests and merging of [8836](https://github.com/TEAMMATES/teammates/pull/8836).
- [x] Researched into implementation of search feature for instructor help page.

Week 7 retrospect:
This week involved finishing the drag and drop functionality for all question types (except Rubric). Everything was ready for review but later merge conflicts were reported again due to another contributor working on enhancing MCQ questions as well. I started researching into the implementation of a search feature for instructor help page.

Week 8 Plan:
- [ ] Create mockups for search feature
- [ ] Implement initial working prototype of search feature
- [ ] Code review and fix merge conflicts with earlier PRs

Week 9 Plan:
- [ ] Buffer period to resolve pending issues from week 6-8
- [ ] Optimize search function to return more relevant results
- [ ] Add tests for search feature 

Week 10 Plan:
- [ ] Back end development (if any) for getting started guide
- [ ] Write back end tests 

Week 11 Plan:
- [ ] Code review + fix issues for getting started guide
- [ ] Improve documentation structure (split into multiple pages + add side navigation where necessary, to be discussed)

Week 12 Plan:
- [ ] Write tests for changes to documentation structure (if any)
- [ ] Fix issues after code review

Week 13 Plan:
- [ ] Buffer period to resolve pending work from week 9-12
- [ ] Code review + Fix issues

Week 14 Plan:
- [ ] Buffer period to resolve pending work from week 9-12
- [ ] Code review + Fix issues
