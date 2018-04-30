# Opening a Pull Request (PR)

These are some basic general rules for creating PRs (pull requests) in git, plus some EOS specific ones.

1. Use the **WIP:** prefix in the name of the PR if the branch you have opened is not yet ready to be merged but you want to:
  a. Ask someone to review some particular part of the code/implementation. In this case, don't expect the person to make a full review since your code is not 100% and he/she will have to make a full review after the **WIP:** prefix is removed.
  b. You want to test that CI is green as you continue making commits to the branch. In this case, please make sure you only do it for a limited time and only when your branch is closer to be finished, otherwise, you will be slowing down the CI queue for other PR in vain.

2. Use as a suffix the ID of the trello card you are working on, e.g.: **Create documentation for delivery strategy. 3**, where 3 is the ID of the card in trello:  https://trello.com/c/Q4o4qz67/3-implement-and-document-a-non-disruptive-delivery-strategy. This will help us in a future identify the PR that solved a specific card in our Roadmap.

3. Run `npm run test:all` before you create a PR to make sure your code is in good shape. Gitlab CI will double check again, but for the sake of making the pipeline run faster, we encourage you to always test locally first.

4. Request someone to review your PR. Depending on the nature of your PR, whether you are modifying just code, or code and UI, you will need the approval from a UX/UI designer or a developer, or both. 
  - People allowed to approve code: Richa Bisht, Cynthia Sanchez, Jesus Herman. 
  - People allowed to approve UX/UI: if you are implementing a design that was already designed by someone, you must request the approval of the same designer. If you are making changes/fixed in the UI/UX yourself, you can request approval to: Cynthia Sanchez, Manuele Carlini, Kenneth Wimer.

5. On top of the UX/UI or code approval, you will need the approval of PO (Cynthia Sanchez) or PO deputy (Kenneth Wimer)

# Being assigned to a PR, approving it, and Mergin to Master

When being assigned to a PR, you must:
- Verify the work done in the UI, by pulling the changes and running the server locally to then be able to verify the implementation satisfies all requirements in the UI.
- Verify the code has no errors and suggest improvements, when possible.
- Sass-lint checks for most of our rules to be applied consistently against our documentation, but the following rules need to be verified manually, so always consider checking these rules are followed:
  - https://gitlab.com/SUSE-UIUX/eos/wikis/Editing-css-style-guide#using-css-preprocessors
  - https://gitlab.com/SUSE-UIUX/eos/wikis/Editing-css-style-guide#javascript-hooks
  - https://gitlab.com/SUSE-UIUX/eos/wikis/Editing-css-style-guide#vendor-prefixed-auto-prefixes
  - https://gitlab.com/SUSE-UIUX/eos/wikis/Editing-css-style-guide#hover-and-focus

For every issue you find you should **Start a discussion** from the comments interface or by writting a comment inline in the code written.

Only once all issues are resolved, you can approve the merge request by clicking on the green button so then the person who initially opened the PR can **merge it to master**.