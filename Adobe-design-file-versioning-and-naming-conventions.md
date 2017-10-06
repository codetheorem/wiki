## Versioning System
All file versioning and backup will be done via git. An automatic mirroring system has been configured to copy the git repository to another service for backup purposes

### Working Space
The main repository for our Adobe files is in github: 
https://github.com/SUSE/EOS/

All work (completed and WIP) will be pushed to this git repository on github. 

Another repository (see below) will automatically copy this git repository as a backup.
      
### Automatic Backup

An automatic backup of the main git repository (mentioned above) will be created at regular intervals thanks to gitlab.com's automatic mirroring functionality.

### Limitations
There is one limitation of this approach. The mirroring will time-out if the process takes longer than 15min.

If this should become an issue we will use a dual push via the .git/config file as follows:

```
[remote "BOTH"]
	url = https://github.com/SUSE/EOS.git
	url = https://gitlab.com/SUSE-UIUX/eos/EOS-PS-SOURCE.git
```

