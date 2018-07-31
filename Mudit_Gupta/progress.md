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
- [ ] Mockups for enhancements to Getting started guide
- [ ] Develop use cases/user stories + UI workflows for enhancements to Getting started guide
- [ ] (In depth discussion to ensure common ground on design)

Week 7 Plan:
- [ ]
- [ ] Front end development for enhancements to Getting started guide
- [ ] Writing Selenium tests

Week 8 Plan:
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
Initial part of this week went into implementing drag and drop feature for Rubric questions. However, I faced a lot of complications
and the plugin I was using until now wasn't working very well for Rubric questions due to their complex structure. The UI was very glitchy and I wasn't able to find a straight forward way to get around it so I decided to keep this issue on hold and move on to the
search feature instead. The remaining week went into developing the core of the search feature which included indexing the documents and
undersstanding how elasticlunr works. By the end of the week I had a working prototype ready for review.

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
- [x] Code review + fix issues with search feature

Week 10 Work:
- [x] Looked into the issues pointed by Cara particularly regarding the pitfalls of using stemming during indexing phase. Looked
into how the Porter stemmer works and experimented by removing the stemmer completely from the search logic to see how does it affect
the results returned and their ranking. In a nutshell I found that removing stemming returns exact matches but at the same time also eliminates relevant results that could be potentially useful.

Week 10 retrospect:
I wasn't able to write much code this week due to it being graduation week and my parents visiting me so I tried to utilise my time 
by researching into issues pointed out in code review.

Week 11 Plan:
- [x] Finish work on search feature
- [x] Code review + fix pending issues in previous PRs

Week 11 Work:
- [x] Finished work on search feature in this week. Added tests, made the pagination system responsive and fixed the highlighting feature due to bugs in previous implementation. Ready for review: PR [Instructor: Help page: Documentation search feature](https://github.com/TEAMMATES/teammates/pull/8951)
- [x] Fixed issues for drag and drop PRs and merged all of them into the MCQ branch [8889](https://github.com/TEAMMATES/teammates/pull/8889). Ready for final review and merging.
- [x] PR [Student: Feedback submission: Rank question: Improve explanation regarding ranking constraints](https://github.com/TEAMMATES/teammates/pull/8870). Ready for final review and merging.
- [x] Due to a failing corner case in PR [Student: submit responses: use a more friendly way to choose evaluee](https://github.com/TEAMMATES/teammates/pull/8878) work was still ongoing.

Week 11 retrospect:
Finished all work on search feature and made it ready for review. Also fixed outstanding issues with previous PRs and made them ready for merging.

Week 12 Plan:
- [ ] Work and finish issue [Instructor: Feedback Session: Improve display of more information for advanced settings #8932](https://github.com/TEAMMATES/teammates/pull/9001)
- [ ] Add some new questions to Instructor help page (still in discussion)
- [ ] Fix issues after code review

Week 13 Plan:
- [ ] 
- [ ] Buffer period to resolve pending work from week 9-12
- [ ] Code review + Fix issues

Week 14 Plan:
- [ ] 
- [ ] Buffer period to resolve pending work from week 9-12
- [ ] Code review + Fix issues
