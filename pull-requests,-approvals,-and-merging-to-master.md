# Opening a Pull Requests

These are some basic general rules for creating PRs (pull requests) in git, plus some EOS specific ones.

1. Use the **WIP:** prefix in the name of the PR if the branch you have opened is not yet ready to be merged but you want to:
  a. Ask someone to review some particular part of the code/implementation. In this case, don't expect the person to make a full review since your code is not 100% and he/she will have to make a full review after the **WIP:** prefix is removed.
  b. You want to test that CI is green as you continue making commits to the branch. In this case, please make sure you only do it for a limited time and only when your branch is closer to be finished, otherwise, you will be slowing down the CI queue for other PR in vain.

2. Use a suffix the ID of the trello card you are working on, e.g.: **Create documentation for delivery strategy. 3**, where 3 is the ID of the card in trello:  https://trello.com/c/Q4o4qz67/3-implement-and-document-a-non-disruptive-delivery-strategy. This will help us in a future identify the PR that solved a specific card in our Roadmap.