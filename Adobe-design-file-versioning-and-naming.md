## Versioning System
All file versioning and backup will be done via git. An automatic mirroring system has been configured to copy the git repository to another service for backup purposes.

### Working Space
The main repository for our Adobe files is in github: 
https://github.com/SUSE/eos-backup

All work (completed and WIP) will be pushed to this git repository on github. 

Another repository (see below) will automatically copy this git repository as a backup.

### Automatic Backup

An automatic backup of the main git repository (mentioned above) will be created at regular intervals thanks to gitlab.com's automatic mirroring functionality.

The mirrored repository can be found here: 
https://gitlab.com/SUSE-UIUX/eos-backup

In gitlab's repository settings for this repository the option "Pull from external source" has been configured.

#### Limitations
There is one limitation of this approach. The mirroring will time-out if the process takes longer than 15min.

If this should become an issue we will use a dual push via the .git/config file as follows:
```
[remote "BOTH"]
	url = https://github.com/SUSE/eos-backup.git
	url = https://gitlab.com/SUSE-UIUX/eos-backup.git
```
__Note: Do not push to the gitlab repository. Doing so will inactivate the automatic mirroring described above__

By adding a remote as given above to the .git/config of the repository calling ```git push BOTH``` will push to the repositories defined sequentially. In this case, calling anything other than "git push BOTH" will lead to the repositories no longer being in sync. 
 

## Naming Conventions
Naming conventions help provide a consistent way to find content at a glance. Consistency within the project is vital. Follow the rules below for naming Adobe files as well as the assets produced from them.

* Do not use capital letters.
* Do avoid "special" characters (: / \ ¢ ™ $ ® [ ] { } ( ) ! ; " ' * ? < > |) and never use spaces, tabs, new lines and embedded returns.
* Do use consistent names for all assets named after what they represent.
* Do match the assets file name to the naming in the source file (group name or layer name, etc.) Being consistent is important in order to improve clarity when looking for a specific item in a psd file.
* Do name all source files after the conceptual piece(s)/component they contain. Examples are "header", "footer", etc.
* Do name files using hierarchy within components. Periods will be used for separating component hierarchy. For example  "main_component.more_specific_component_name".
* Do separate words within one conceptual piece/component. Underscores will be used for separators between words which describe a conceptual piece/component itself. Examples are "header.user_login.psd",  "main_navigation.dropdown_menu.psd", or "main_navigation.accordion.psd".
* Do use a dash "-" to reflect state. Examples are "button-hover" or "checkbox-on".
* Do add the postfix "WIP" to a filename to save work which is unfinished. Only one "WIP" file should be created for a given name.

