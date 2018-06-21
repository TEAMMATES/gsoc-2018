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
- [ ] Code Review

Week 7 Plan:
- [ ] Code Review

Week 8 Plan:
- [ ] Implement the ability for respondents to add comments for numerical-scale questions
- [ ] Implement the ability for respondents to add comments for MSQ questions
- [ ] Implement the ability for respondents to add comments for rank questions
- [ ] Update UI for response comments
- [ ] Add tests for trio

Week 9 Plan:
- [ ] Implement the ability for respondents to add comments for rubric questions
- [ ] Implement the ability for respondents to add comments for distribute questions
- [ ] Update UI for response comments
- [ ] Add tests for both

Week 10 Plan:
- [ ] Ability for instructors to add comments from view, Giver > Question > Recipient.
- [ ] Ability for instructors to add comments from view, Recipient > Question > Giver
- [ ] Add tests for both

Week 11 Plan:
- [ ] Finish any remaining work from week 8-10
- [ ] Fix issues after code review
- [ ] Implement backend of ability for instructors to disable comments

Week 12 Plan:
- [ ] Implement frontend of ability for instructors to disable comments
- [ ] Add tests

Week 13 Plan:
- [ ] Code review and code fix

Week 14 Plan:
- [ ] Code review and code fix
