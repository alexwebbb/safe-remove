# General Notes

- deleted files go to $HOME/deleted
- program is literally "remove"
- files restored using script called "restore". when file is restored, entry is removed from record

## Error Conditions

- file does not exist
- no filename
- file is a directory, but only if -r is not supplied (not relevant to restore)
- cant delete the remove script itself

## File Types

- deleted files will have the format filename_inode
- deleted file info is stored in .restore.info, which will be in the home folder
- file info is stored as filename_inode:/full/path

+ if additional stored data componenets are handled, external file indexed by inode
+ maybe something like ".restore.detail"

## Syntax 

- call will be sh remove "filename"
- similarly, call to restore will be sh restore "filename", of course considering the name now includes the inode
- must support interactive via -i, just like rm
- must support verbose via -v, just like rm
- must support recursive deletion via 

+ potentially a syntax for reviewing deleted files, like -l to list, and -d for date range

## Push Goals

- handle and store read / write permissions
- store date and command to review file history by date
- store and handle date modified using touch
- dialogs?? 
