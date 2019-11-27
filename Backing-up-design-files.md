[Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#designing-the-eos-project)


1. [Process](#process)
2. [How does the versioning system work?](#how-does-the-versioning-system-work)
3. [Naming Conventions](#naming-conventions)

## Process

Whenever your work involves creating a design file in Photoshop, Illustrator, Adobe XD, Premiere, or others, you should follow the following steps in order to properly save your files:

For every iteration you make on your design you should make a git commit saving the current version to Gitlab. To explain it better we will use an example case:

1. You are working on a design for a new logout page. You will normally work on a few proposals, those proposals should all be included in the same XD file. When you are ready to show your design ideas to the team for some feedback you should make a commit saving that current state (before applying changes suggested by team members). 

2. You now have received some suggestions and you have marked some options as *rejected* and updated others. This is another iteration on your file and you should make a new commit to keep these new options in the history of the file. 

3. After a new round of feedback, and having your design finally approved, you are ready to commit the final file to the eos-backup repository. At this point, you should make sure to remove all rejected designs and leave only the approved design, then make your commit to Gitlab. 

## How does the versioning system work?
All file versioning and backup will be done via git.

### Working Space
The main repository for our Adobe files is in Gitlab: 
https://gitlab.com/SUSE-UIUX/eos-backup

All work (completed and WIP) will be pushed to this git repository. 

Git allows us to go back to previous changes of a file as long as you carefully took care of following the process defined above. 

## Naming Conventions
Naming conventions help provide a consistent way to find the content at a glance. Consistency within the project is vital. Follow the rules below for naming Adobe files as well as the assets produced from them.

* Do not use capital letters.
* Do avoid "special" characters (: / \ ¢ ™ $ ® [ ] { } ( ) ! ; " ' * ? < > |) and never use spaces, tabs, new lines and embedded returns.
* Do use consistent names for all assets named after what they represent.
* Do match the assets file name to the naming in the source file (group name or layer name, etc.) Being consistent is important in order to improve clarity when looking for a specific item in a psd file.
* Do name all source files after the conceptual piece(s)/component they contain. Examples are "header", "footer", etc.
* Do name files using hierarchy within components. Periods will be used for separating component hierarchy. For example  "main_component.more_specific_component_name".
* Do separate words within one conceptual piece/component. Underscores will be used for separators between words which describe a conceptual piece/component itself. Examples are "header.user_login.psd",  "main_navigation.dropdown_menu.psd", or "main_navigation.accordion.psd".
* Do use a dash "-" to reflect the state. Examples are "button-hover" or "checkbox-on".
* Do add the postfix "WIP" to a filename to save work which is unfinished. Only one "WIP" file should be created for a given name.


