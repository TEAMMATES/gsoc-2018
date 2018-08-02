# Mudit Gupta

**Project: Usability Hero**

Overall Direction:
- Provide Context specific help
- Improve Getting Started guide
- Improve documentation structure
- Sidebar for sections of instructor help (to be discussed)
- Resolve UI/UX issues

---

Week 1 Plan:
- [ ] 
- [ ] Work on [Student: feedback submission: distribution points question: explain if equal points are not allowed](https://github.com/TEAMMATES/teammates/issues/8817)
- [ ] Discuss with Cara further work to be done on Getting started guide and help docs

Week 2 Plan:
- [ ] Front end development for sidebar of instructor help (to be discussed)
- [ ] UI Enhancements for Distribute points style questions
- [ ] Write browser tests for enhancements

Week 3 Plan:
- [ ] Solve UX issues on the side
- [ ] Simplify views for complicated tasks by hiding details/advanced options
- [ ] Write tests for new views

Week 4 Plan:
- [ ]
- [ ] Finding remaining views that need simplification and fixing those
- [ ] Write remaining tests

Week 5 Plan:
- [ ]
- [ ] Buffer period to resolve pending work from week 1-4
- [ ] Fix issues after code review

Week 6 Plan:
- [ ] Mockups for enhancements to Getting started guide (scrapped)
- [ ] Develop use cases/user stories + UI workflows for enhancements to Getting started guide (scrapped)
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
- [ ] Front end development for enhancements to Getting started guide (scrapped)
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
- [ ]
- [ ] Back end development (if any) for getting started guide
- [ ] Write back end tests 

Week 11 Plan:
- [ ] 
- [ ] Code review + fix issues for getting started guide
- [ ] Improve documentation structure (split into multiple pages + add side navigation where necessary, to be discussed)

Week 12 Plan:
- [ ]
- [ ] Write tests for changes to documentation structure (if any)
- [ ] Fix issues after code review

Week 13 Plan:
- [ ] 
- [ ] Buffer period to resolve pending work from week 9-12
- [ ] Code review + Fix issues

Week 14 Plan:
- [ ] 
- [ ] Buffer period to resolve pending work from week 9-12
- [ ] Code review + Fix issues
