## Versioning System
All file versioning and backup will be done via git. An automatic mirroring system has been configured to copy the git repository to another service for backup purposes

### Working Space
The main repository for our Adobe files is in github: 
https://github.com/SUSE/EOS/

All work (completed and WIP) will be pushed to this git repository on github. 

Another repository (see below) will automatically copy this git repository as a backup.

### Automatic Backup

An automatic backup of the main git repository (mentioned above) will be created at regular intervals thanks to gitlab.com's automatic mirroring functionality.

#### Limitations
There is one limitation of this approach. The mirroring will time-out if the process takes longer than 15min.

If this should become an issue we will use a dual push via the .git/config file as follows:
```
[remote "BOTH"]
	url = https://github.com/SUSE/EOS.git
	url = https://gitlab.com/SUSE-UIUX/eos/EOS-PS-SOURCE.git
```
_Note: The url's above are only placeholders._

By adding a remote as given above to the .git/config of the repository calling ```git push BOTH``` will push to the repositories defined sequentially. 
 

## Naming Conventions
Naming conventions help provide a consistent way to find content at a glance. Consistency within the project is vital.

* Do use consistent names for all assets named after what they represent and do match the assets file name to the naming in the source file (group or layer, etc.)
* Do name all source files after the conceptual piece(s) they contain. Examples are header, footer.
* Do name all source files
* Do not use capital letters 
* Underscores will be used for file name separators within  conceptual pieces. Example: main_navigation

