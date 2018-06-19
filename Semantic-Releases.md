## This project uses Semantic-release 

[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

Github: https://github.com/semantic-release/semantic-release/

### Semantic commit messages that will update the npm package version:

We follow ESlint version conventions. They base their release numbers on git commit tags (tags are the first word in the commit message followed by a colon, eg: `Fix: bug in main menu`). These tags are: `Breaking:`, `Update:`, `New:`, and `Fix:`, and they should always be followed by a commit message.

Here is an example of the release type that will be done based on a commit message:

| Commit message                                                                                                                                                                                   | Release type               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| `Breaking: change class name for all EOS icons`                                                                                                                             |  Major Release - a version that will break something in the user application after updating the package              |
| `Update: change design of bootstraping icon` | Minor Release - a version that changes things in the package without the need from the user to modify the code base  |
| `New: create a login icon` | Minor Release - a version that adds new components that wont damage the existing ones|
| `Fix: remove 1px space in systems icon`                                                                                                                                                     | Patch Release - a version that wont break anything or add any new feature after updating, just fixes a bug |



More information about semantic releases: https://semver.org/