# Using the slash character in Git branch name

When creating a new branch in git, you need to use the slash character to separate the **Theme** / **name-of-branch**.
By **Theme** we mean you need to use one of the 6th different themes (or Trello labels) the EOS roadmap uses: https://trello.com/b/PauX7Rel/eos-roadmap-backlog.
They are:
1. ui
2. ux
3. ops *(don't use **operations**, gitlab seems to have conflicts letting you push folders with that name)*
4. engagement
5. training
6. front-end

The Theme and Branch name should always be in lowercase and for the branch name if it contains more than 1 words in it, use minus (-) to separate them, eg: **ui/collapsable-notifications**

This theme will be easy for you to find out since it will be part of the card you are working on. If the card you are working on has no theme, then this card is not properly following the **Definition of Ready** and it should be moved back to the backlog column **New cards**

Using the slash character to separate Theme and Branch-name will, in the end, be detected by most git software, as a directory/file format, improving the browsing of extensive lists of branches for later review.

## Using Fork for Mac?

Download from: https://git-fork.com/

If you do, you will notice that using the slash character when naming branches makes it very easy to navigate through branches since it will show you folders for all the pre-slash names, themes in our case. In fork you will see something like this:

![image](/uploads/400f5b5bd2168c776a69f245f2b05caa/image.png)

# Avoid conflicts

Names need to be unique. For example, you can't have both a file and a directory with the same name. This means you should never name a branch simply **UX** because it will cause conflicts with all the other branches that are named **UX/branch-name**, **UX/main-navigation**, etc.