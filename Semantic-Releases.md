◀️ [Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#releases)


# This project uses Semantic-release 

[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

Github: https://github.com/semantic-release/semantic-release/

## Semantic commit messages that will update the project version:

We follow ESlint version conventions. They base their release numbers on git commit tags (tags are the first word in the commit message followed by a colon, eg: `Fix: bug in main menu`). These tags are: `Breaking:`, `Update:`, `New:`, and `Fix:`, and they should always be followed by a commit message.

Here is an example of the release type that will be done based on a commit message:

| Commit message                                                                                                                                                                                   | Release type               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| `Breaking: change class name for all EOS icons`                                                                                                                             |  Major Release - a version that will break something in the user application after updating the package              |
| `Update: change design of bootstraping icon` | Minor Release - a version that changes things in the package without the need from the user to modify the code base  |
| `New: create a login icon` | Minor Release - a version that adds new components that wont damage the existing ones|
| `Fix: remove 1px space in systems icon`                                                                                                                                                     | Patch Release - a version that wont break anything or add any new feature after updating, just fixes a bug |

More information about semantic releases: https://semver.org/

### When to create a release commit?

We should continue creating normal commits in our branches, with the exception that if the card has a request from PO to create a release, then we need to modify the commit message of the Pull Request (all normal commits continue being the same).

PO will request the type of release for the PR: Patch, Minor, Major.


### How to modify the commit message of a PR to create a release

When you open a PR and save it, you will see the following:

![image](/uploads/8e83b8c47abe2c77acca43d344dde8dc/image.png)

Clicking on "Modify commit message" opens an input field that will let you modify the normal **Merge branch XXX into master** type of commit message of PRs.
There, you need to modify the commit message (when required by the PO in the card) for the type of release this PR should create, for example:

![image](/uploads/6427524ff538078cb7b5787c36f6ecc1/image.png)

That will create a Minor release when merged into master.



