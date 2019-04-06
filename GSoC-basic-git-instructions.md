### How to open PRs to EOS or EOS-icons:

1- In order to open PRs in any open source project, you have to fork the repository. Forking it will create a new repository under your user and link it to the original repository you forked it from. In this case EOS or EOS-icons so Gitlab will be able to detect changes in your repository and offer you to open a PR against origin.

2- The best practice is to NEVER work on your master, but instead create branches in your repo. Why? because your master should always be 1:1 with our master, this way you can update your master whenever another developer merges something into EOS/EOS-icons master, and your repo doesn't get outdated.

3- Create a new branch in your repository by typing `git checkout -b 'name-of-the-branch'`. You must execute this command being in master, and having your master clean. This command will create the new branch, and checkout you to that new branch, all at once.

4- When you finished with your branch and you think it is ready to be merged, push your commits and head to Gitlab, you will see a blue link that offers you to open a PR. There, you need to select our Master branch and the PR will be opened.

5- Once the PR is opened, someone in the EOS team will be assigned to review your PR. However, please ping us here to make sure someone is checking it. Once approved, we will merge it.


### How to update your Master branch

I've made changes in CI in EOS and EOS-icons so you should update your `master` branches. To do so first make sure you didn't make any changes in your master. If you did, I suggest that you fork the repo from scratch and start over.

If your `master` branch is clean, to update it you have to do the following:

##### Configure your local git

1- Add upstream (you only need to do this once) `git remote add upstream git@gitlab.com:SUSE-UIUX/eos.git` (**)

2- Verify it went well: `git remote -v`. You should see

```
origin    git@gitlab.com:YOUR-USERNAME/eos-icons.git (fetch)
origin    git@gitlab.com:YOUR-USERNAME/eos-icons.git (push)
upstream    git@gitlab.com:SUSE-UIUX/eos-icons.git (fetch)
upstream    git@gitlab.com:SUSE-UIUX/eos-icons.git (push)
```

##### Now you are ready to fetch and merge, every time you start a new branch you should do:

1- `git checkout master`

2- `git fetch upstream`

3- `git merge upstream/master`

##### That's it!.. your `master` branch is updated with EOS

(**) to do this with EOS-icons, the process is the same but you should do it with EOS-icons repo `git@gitlab.com:SUSE-UIUX/eos-icons.git`

### How to merge Upstream Master into the branch you are currently working on

1- First, you need to merge Upstream Master into your local Master by following the steps above (**How to update your Master branch**).

2- Checkout back into your branch with `git checkout YOUR_BRANCH_NAME`.

3- Merge Master into your branch with `git merge master`.

4- You will possibly have merge conflicts to fix if the files you are modifying in your branch have been modified in Upstream Master. You need to carefully pay attention to what changed in Master and what you changed, and cleanup the code accordingly. If you are having problems understanding how Merge conflicts work, please watch the following video to have a better understanding: https://youtu.be/1MVQYSlgXrI