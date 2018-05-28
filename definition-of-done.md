# Definition of done
Look at the initial inputted user task. It was likely optimized, clarified to remove any possible ambiguity. Once the requirements have been
massaged and optimized the design for how the tasks may be implemented are enumerated and weighed. Don't forget simple unit testing and
security vetting is not merely extra credit, if you haven't done them...you haven't done your job!

For a ticketing system having different statuses to represent the progress of a given item shows transparency for the team and PO. You need to
pick conventions that work for your team and project. Here are some possible approaches:

1. Requirement captured
2. Requirement optimized
3. Requirement accepted/rejected
4. Design process and enumerate different implementation options
5. For each design provide:
    1. LOE on implementation
    2. Known security vulnerabilities, or if this is the preferred security approach
    3. Rate the "cleanest" approach via code quality, modularity
    4. Express if this approach is somehow similar or different than other similar tasks. The best approach is sometimes the more
familiar. There is value to that, indicate that this may or may not be the "best" way of implementing a given task, but is consistent
with the rest of the system and therefore a better approach
    5. Are there different execution impacts? Longer, shorter, slightly less feature-rich
    6. Do the different approaches have different monetary cost implications? More resource hungry?
    7. Ease of testing for success, failure, and edge conditions
6. Indicate the design chosen and a brief reason why.
7. Create a threat model.
    1. Show current system state with a data flow diagram.
    2. Add in the change to the system with the new functionality.
    3. Enumerate all possible threats that had existed before as well as additional threats.
    4. For each threat provide at least one compensating control to mitigate the threat
    5. Compare and contrast if the added functionality outweighs any remaining possible threats even with the compensating controls.
8. A branch should be created that reflect the ticket number
9. Initial technical task supports described functionality
10. Positive, negative, and edge case unit tests are present
11. Positive, negative, and edge case functional tests are present
12. Security tests are in place to ensure that compensating controls are working and mitigate the threat.
13. Any infrastructure, or migration related matters must be capable of being run upon deployment without any human interaction
14. Ready for peer code review. A pull request should be submitted. Indicating the ticket number with a brief description of the changes
present
15. Code review should show that only code present in committed code reflect the ticket at hand. The code review should not be taken
lightly. That person is now responsible for bad code just as much as the engineer who authored it. Don't just accept the request, add
some comments.
16. An attempt will be made to merge in the new branch into the master code base. Should requisite tests, code coverage, and other related
tests pass the merge should apply and accept the code.
17. The merge into the master branch should trigger a new deployment into the corresponding environment.
