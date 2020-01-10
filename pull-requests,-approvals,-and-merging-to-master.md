◀️ [Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#git)


## Opening a Pull Request (PR)

These are some basic general rules for creating PRs (pull requests) in git, plus some EOS specific ones.

1. Use the **WIP:** prefix in the name of the PR if the branch you have opened is not yet ready to be merged but you want to:
  a. Ask someone to review some particular part of the code/implementation. In this case, don't expect the person to make a full review since your code is not 100% and he/she will have to make a full review after the **WIP:** prefix is removed.
  b. You want to test that CI is green as you continue making commits to the branch. In this case, please make sure you only do it for a limited time and only when your branch is closer to be finished, otherwise, you will be slowing down the CI queue for other PRs in vain.

2. Run `npm run test:all` before you create a PR to make sure your code is in good shape. Gitlab CI will double check again, but for the sake of making the pipeline run faster, we encourage you to always test locally first.

3. Use one of the [templates documented here](/PR-templates) for your PR. Please be as thorough as possible.

4. Our Meggie bot will assign someone to open PRs to review your code. Add the person that got assigned in Gitlab. If the person is either yourself or a person out of the office, close and re-open the PR to get a new assignee. If the PR was about implementing a designer's design, make sure you show it to s/he and get her/his approval too.

5. The PR should have `master` as a target and never trigger a release unless the card specifies it. The PO will check when a card is concluding an epic and requires to launch a new release. More info about how to trigger releases [https://gitlab.com/SUSE-UIUX/eos/wikis/Semantic-Releases]

## Being assigned to a PR, approving it, and merging to master

When being assigned to a PR, you must:
- Verify the work done in the UI, by pulling the changes and running the server locally to then be able to verify the implementation satisfies all requirements in the UI.
- Verify the code has no errors and suggest improvements, when possible.
- If you find a simple bug, even if it is not part of the PR the colleague opened, make sure you mention it. The developer can decide to either fix it in the same PR or open an issue so someone else takes care later.
- Sass-lint checks for most of our rules to be applied consistently against our documentation, but the following rules need to be verified manually, so always consider checking these rules are followed:
  - https://gitlab.com/SUSE-UIUX/eos/wikis/Editing-css-style-guide#using-css-preprocessors
  - https://gitlab.com/SUSE-UIUX/eos/wikis/Editing-css-style-guide#javascript-hooks
  - https://gitlab.com/SUSE-UIUX/eos/wikis/Editing-css-style-guide#vendor-prefixed-auto-prefixes
  - https://gitlab.com/SUSE-UIUX/eos/wikis/Editing-css-style-guide#hover-and-focus

For every issue, you find you should **Start a discussion** from the comments interface or by writing a comment inline in the code written.

Only once all issues are resolved, you can approve the merge request by clicking on the green button so then the person who initially opened the PR can **merge it to master**.

**Please make sure that you delete the branch once it merges**.

## Deploying to production.

Once CI has passed after a successful merge into master, Gitlab CI will give the option to manually deploy to production. This should only be made after having properly checked the staging server [undisclosed for security reasons] and by the PO [@cyntss] or acting deputy.

