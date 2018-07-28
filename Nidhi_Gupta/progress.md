# Nidhi Gupta

**Project: Comments for Responses**

Overall Direction:
- Ability for respondents to add comments for their own responses in following question types.
    * Multiple-choice (single answer) question
    * Multiple-choice (multiple answers) question
    * Numerical-scale question
    * Distribute points (among options) question
    * Distribute points (among recipients) question
    * Rubric question
    * Rank (Options) question
    * Rank (Recipients) question

- Ability for instructors to add comments from more places.
	* Giver > Question > Recipient
	* Recipient > Question > Giver

Bonus features (To do after adding basic comment feature for all question types)
- Allow instructors to disable comments.
- Ability to know if the comment was read.
- Allow instructors to require comments.

---

Week 1 Plan: 
- [x] Implement the backend part of the ability for respondents to add comments for MCQ questions
- [x] Implement the frontend part of comments feature for students

Works
- 1st review ready at https://github.com/TEAMMATES/teammates/pull/8830#issuecomment-391105329

Retrospect on Week 1:
Most of the week 1 went into understanding the comments feature for instructors and implementing the same for students.
Previous closed PR on this issue helped a lot in this regard. 
I learnt working with JSP and tag files. There were instances when I felt I had completely broken the project.
Debugging was the hardest part in this week.

Week 2 Plan:
- [x] Accomodate student comments in instructor results page (All views)
- [x] Implement the ability to edit and delete comments

Works
- 2nd review ready at https://github.com/TEAMMATES/teammates/pull/8830#issuecomment-392290459

Retrospect on Week 2:
Week 1 made me quite comfortable to make further changes. This was the week when I made lots of changes in the code owing to dreaded Null Pointer Exception.
I spent a day trying to figure out reason for Malformed Url Exception but in vain. Finally I left it as it is and continued make other changes. Somehow surprisingly this error went away after few commits in travis build but not on my development environment. 
I think I spent more time debugging my code than actually adding new code. So I learnt to be more careful while writing code to avoid mistakes that would cost me much more time because of debugging.

Week 3 Plan:
- [x] Add comments column to CSV 
- [x] Add tests for MCQ

Works
- 3rd review ready at https://github.com/TEAMMATES/teammates/pull/8830#issuecomment-393665433

Retrospect on Week 3
Adding tests was easiest part. I spent most of the time fixing the failing tests. I felt that in last three weeks, reviews were not as consisent as thought it would be. I believe this was due to unavailability of senior mentor. 
I utilised this time to try improve my code. I really enjoyed testing the new feature and I am looking forward to getting this PR merged by next week.

Week 4 Plan:
- [x] Finish any remaining work from week 1-3
- [ ] Fix issues after code review

Works
- Opened new issue and PR [Instructor: comment on responses: support entering comments for each response from view GQR #8872](https://github.com/TEAMMATES/teammates/pull/8897)

Retrospect on Week 4:
Code review couldn't be done in this week so I worked upon feature to support entering comments for each response from view Giver-Question-Recipient which was to be done in Week 10. It is almost done. Adding tests is remaining.

Week 5 Plan:
- [ ] Implement the ability for respondents to add comments for numerical-scale questions
- [ ] Implement the ability for respondents to add comments for MSQ questions
- [ ] Implement the ability for respondents to add comments for rank questions
- [ ] Add tests for trio

Works
- Merged PR [Instructors: sessions page: fix 'resend link to view results'](https://github.com/TEAMMATES/teammates/pull/8827)
- 3rd review ready [Student: view results: rank questions: show average](https://github.com/TEAMMATES/teammates/pull/8784#issuecomment-397224861)

Retrospect on Week 5:
First half of the week I majorly worked upon above mentioned PRs. I got review on main ongoing PR in second half of the week. I learnt I should remember to add Javadoc for majority of new functions that I add. There were some major changes suggested by mentor Xiao, which will take some time to implement. Since the PR is huge, many iterations of review is expected. I couldn't complete this week's plan because I underestimated the time required for reviewing and fixing code after that.

Week 6 Plan:
- [x] Code Review

Works
- Worked majorly upon fixing code after reviews.

Retrospect on Week 6:
This week had a steep learning curve. Through code reviews, I learnt better coding practices. There were no major roadblocks.

Week 7 Plan:
- [x] Code Review

Works
- Worked majorly upon fixing code after reviews.
- Review ready PR [Instructor: comment on responses: support entering comments for each response from view GQR #8872](https://github.com/TEAMMATES/teammates/pull/8897)
- Opened PR [Instructor: Question view: visibility icon does not appear for new comments #8899](https://github.com/TEAMMATES/teammates/pull/8934)

Retrospect on Week 7:
Code looks clean now. I guess it would take some more time to get the main PR merged. I plan to work on this along with other issues related to comments feature.

Week 8 Plan:
- [x] Code Review
- [x] Ability for instructors to add comments from view, Giver > Question > Recipient
- [x] Add tests
- [x] Work on adding visibility icon to all comments

Works
- Review ready PR [Instructor: Question view: visibility icon does not appear for new comments #8899](https://github.com/TEAMMATES/teammates/pull/8934)

Retrospect on Week 8:
I faced two difficulties this week. First one, I encountered lots of unrelated errors after pulling from master. There were updates in development packages. It was some problem caused by intelliJ. Second being failing test on master branch. My mentors helped me solve both the issues quickly so that time is not wasted. And both of them were related to intelliJ. Apart from this, no other major setbacks.

Week 9 Plan:
- [x] Fix backward compatibility issues in #8830 (Comments on responses)
- [x] Improve implementation of #8872 (GQR)

Works
- Merged PR [Instructor: Question view: visibility icon does not appear for new comments #8899](https://github.com/TEAMMATES/teammates/pull/8934)

Retrospect on Week 9:
This week I worked upon making comments on responses PR backward compatible. I enjoyed discussing with mentors about ways we can ensure that legacy data is handled. I saw few of the old data migration scripts which was pretty amazing. I previously thought that data migration is something extremely complicated. But now I wish to write one myself for comments feature in future. In my GQR PR, there were logic holes in my previous implementation which got discovered during review. So I think I need to be more careful and think deeply so as to avoid writing bad logic in future.

Week 10 Plan:
- [x] Separate tag and js files for feedback participant comments feature #8830 (Comments on responses)
- [x] Refactor tests for #8872 (GQR)
- [x] Add tests for #8701 (Show average rank)
- [x] Add unit tests for #8830 (Comments on responses)

Works
- Merged PR [Student: view results: rank questions: show average #8701](https://github.com/TEAMMATES/teammates/pull/8784)

Retrospect on Week 10:
This week I worked upon separating feedback participant comments from instructor comments completely. It simplified the implementation of comment indexes. I also wrote lots of unit tests for all the new methods that I introduced in my multiple PRs. I feel more confident about writing tests at the end of this week. No major difficulties encountered.

Week 11 Plan:
- [x] Modify UI of feedback participant comments feature #7239 (Comments on responses)
- [x] Finish any remaining work from week 8-10
- [x] Ability for instructors to add comments from view, Recipient > Question > Giver

Works
- Merged PR [Instructor: comment on responses: support entering comments for each response from view GQR #8872 ](https://github.com/TEAMMATES/teammates/pull/8897)
- Merged PR [Instructor: comment on responses: support entering comments for each response from view RQG #8987 ](https://github.com/TEAMMATES/teammates/pull/8992)

Retrospect on Week 11:
This week was great. I finished work on supporting entering comments from views GQR and RQG. I gave final touches to main comments PR, which will mostly be approved after few rounds of reviews. No major setbacks.

Week 12 Plan:
- [ ] Code review

Week 13 Plan:
- [ ] Implement the ability for respondents to add comments for numerical-scale questions
- [ ] Implement the ability for respondents to add comments for MSQ questions
- [ ] Implement the ability for respondents to add comments for rank questions
- [ ] Update UI (if required)
- [ ] Add tests for trio

Week 14 Plan:
- [ ] Implement the ability for respondents to add comments for rubric questions
- [ ] Implement the ability for respondents to add comments for distribute questions
- [ ] Update UI (if required)
- [ ] Add tests for both
