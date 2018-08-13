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
<<<<<<< HEAD
- [x] Create mockups for search feature
- [x] Implement initial working prototype of search feature
- [x] Code review and fix merge conflicts with earlier PRs

Week 8 Work:
- [x] Worked on issue [Instructor: Edit rubric question: reorder options using drag and drop](https://github.com/TEAMMATES/teammates/issues/8933) to add drag and drop feature to rubric questions.
- [x] Create mockups for the search function for instructor help documentation. Finalized implementation approach
for the same by discussing with mentors.
- [x] Implemented the first version of the search function that simply searches and displays all relevant 
results. PR [Instructor: Help page: Documentation search feature](https://github.com/TEAMMATES/teammates/pull/8951).

Week 8 retrospect:
Initial part of this week went into implementing drag and drop feature for Rubric questions. However, I faced a lot of complications and the plugin I was using until now wasn't working very well for Rubric questions due to their complex structure. The UI was very glitchy and I wasn't able to find a straight forward way to get around it so I decided to keep this issue on hold and move on to the search feature instead. The remaining week went into developing the core of the search feature which included indexing the documents and understanding how elasticlunr works. By the end of the week I had a working prototype ready for review.

Week 9 Plan:
- [x] Buffer period to resolve pending issues from week 6-8
- [x] Optimize search function to return more relevant results
- [ ] Add tests for search feature 

Week 9 Work:
- [x] Built a highlighting feature for the search function that highlights the keywords of query in the results returned.
- [x] Built a pagination system from scratch that splits the search results into multiple pages for better usability.
- [x] Experimented with different search configurations to optimize results returned.

Week 9 retrospect:
As planned, this week went into enhancing the search feature by adding highlighting and pagination. I also experimented with different boost values which are part of the search configuration passed to elasticlunr. Building the pagination system took longer than i expected which is why I wasn't able to add tests this week.

Week 10 Plan:
- [ ] ~~Back end development (if any) for getting started guide~~ (scrapped)
- [ ] ~~Write back end tests~~ (scrapped)
- [x] Code review + fix issues with search feature

Week 10 Work:
- [x] Looked into the issues pointed by Cara particularly regarding the pitfalls of using stemming during indexing phase. Looked into how the Porter stemmer works and experimented by removing the stemmer completely from the search logic to see how does it affect the results returned and their ranking. In a nutshell I found that removing stemming returns exact matches but at the same time also eliminates relevant results that could be potentially useful.

Week 10 retrospect:
I wasn't able to write much code this week due to it being graduation week and my parents visiting me so I tried to utilise my time by researching into issues pointed out in code review.

Week 11 Plan:
- [x] Code review + fix pending issues in previous PRs
- [ ] ~~Improve documentation structure (split into multiple pages + add side navigation where necessary)~~ (scrapped)
- [x] Finish work on search feature

Week 11 Work:
- [x] Review ready PR: [Instructor: Help page: Documentation search feature](https://github.com/TEAMMATES/teammates/pull/8951). Finished work on search feature in this week. Added tests, made the pagination system responsive and fixed the highlighting feature due to bugs in previous implementation.
- [x] Review ready PR: [Instructor: edit MCQ question: give an easier way to reorder options](https://github.com/TEAMMATES/teammates/pull/8889). Fixed issues for drag and drop PRs and merged all of them into the MCQ branch.
- [x] Review ready PR [Student: Feedback submission: Rank question: Improve explanation regarding ranking constraints](https://github.com/TEAMMATES/teammates/pull/8870).
- [x] Due to a failing corner case in PR [Student: submit responses: use a more friendly way to choose evaluee](https://github.com/TEAMMATES/teammates/pull/8878) work was still ongoing.

Week 11 retrospect:
Finished all work on search feature and made it ready for review. Also fixed outstanding issues with previous PRs and made them ready for merging.

Week 12 Plan:
- [ ] ~~Write tests for changes to documentation structure (if any)~~ (scrapped)
- [x] Work and finish issue [Instructor: Feedback Session: Improve display of more information for advanced settings #8932](https://github.com/TEAMMATES/teammates/pull/9001)
- [x] Fix other UX issues
- [ ] ~~Add some new questions to Instructor help page~~ (awaiting response from Cara)
- [ ] Fix issues after code review and merge PRs

Week 12 work:
- [x] Merged: [Instructor: Add Course title to Student Details page](https://github.com/TEAMMATES/teammates/pull/8861)
- [x] Review ready PR: [Instructor: Feedback Session: Improve display of more information for advanced settings #8932](https://github.com/TEAMMATES/teammates/pull/9001)
- [x] Review ready PR: [Student: submit responses: use a more friendly way to choose evaluee #8867](https://github.com/TEAMMATES/teammates/pull/8878). Fixed the corner case of user using the separating symbol as part of section, team and name fields by passing the fields as separate attributes in HTML.
- [x] Created PR: [Warn if browser is not compatible with TEAMMATES #9011](https://github.com/TEAMMATES/teammates/pull/9016). Initially thought of updating the version numbers as well but it was later decided to completely eliminate them at the moment.
- [x] Fixed unnoticed bugs in PRs awaiting review, cleaned up the code and added screenshots of final changes where required as suggested by Prof Damith.

Week 12 retrospect:
The plan for this week was to review and merge all open PRs. However, due to mentors being busy with their own work that couldn't happen. I discussed the issue with Prof Damith and he suggested to make sure all PRs are as ready as possible, post final screenshots of changes made and deploy to staging server where needed. I used this week to work on new issues and fix bugs that went unnoticed in PRs awaiting review.

Week 13 Plan:
- [x] Buffer period to resolve pending work from week 9-12
- [x] Code review + Fix issues

Week 13 work:
- [x] Merged: [Instructor: Help page: Documentation search feature](https://github.com/TEAMMATES/teammates/pull/8951)
- [x] Approved: [Student: Feedback submission: Rank question: Improve explanation regarding ranking constraints](https://github.com/TEAMMATES/teammates/pull/8870)
- [x] Approved: [Instructor: edit MCQ question: give an easier way to reorder options](https://github.com/TEAMMATES/teammates/pull/8889)
- [x] Awaiting final review and merging: [Instructor: Feedback Session: Improve display of more information for advanced settings #8932](https://github.com/TEAMMATES/teammates/pull/9001)
- [x] Awaiting response: [Student: submit responses: use a more friendly way to choose evaluee #8867](https://github.com/TEAMMATES/teammates/pull/8878). Waiting for response for comment [here](https://github.com/TEAMMATES/teammates/pull/8878#discussion_r208111443) before making final changes. Other issues pointed in review have been fixed.
- [x] Closed: [Instructor: Edit distribute points question: reorder options using drag and drop](https://github.com/TEAMMATES/teammates/pull/8916) since all changes of this PR were merged in [8889](https://github.com/TEAMMATES/teammates/pull/8889)
- [x] Ongoing PR: [Warn if browser is not compatible with TEAMMATES #9011](https://github.com/TEAMMATES/teammates/pull/9016). Currently finalizing designing for a dismissable alert and fixing issues pointed in review.
- [x] Created issue: [Instructor: Edit Feedback Session: Add drag and drop feature for question option weights #9040](https://github.com/TEAMMATES/teammates/issues/9040)

Week 13 retrospect:
I managed to get reviews this week. Majority of the week went into fixing issues after code review. I am still waiting for final reviews on some PRs (mentioned above) that are close to merging. Later half of the week was spent working on newer issues.
=======
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
>>>>>>> master

Week 14 Plan:
- [ ] Buffer period to resolve pending work from week 9-12
- [ ] Code review + Fix issues
