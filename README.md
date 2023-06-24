# Bash Scripts

## This repo is for useful bash scripts

List of scripts:
1. [go](./bookmark_command/)
2. [nts](./bookmark_command/)

## Setup
### To use these scripts globally as commands, paths to the bash scripts must be added to the .bashrc file.

1. Go to ~/ (home directory).
1. Open .bashrc file with admin privilages using sudo or su.
1. Go to the end of the file.
1. Add the path of cloned repo:
```
export PATH="<path to cloned repo>:$PATH"
```
### Give executable permissions to bash files
1. Navigate to the cloned repo and add executable permission to commands.
```
chmod +x go
```
**only the bash files with executable permissions will be able to run**

### For 'go' command add an alias
1. Go to ~/ (home directory).
1. Open .bashrc file with admin privilages using sudo or su.
1. Find alias in .bashrc
1. Add the following alias
```
alias go='. go'
```
**this will stop go command form executing in a child shell**

## Usage

### go
This script will help you navigate to bookmarks in you bash termial, you can also set book marks.

**Make sure the BM_data.txt and path_data.txt are present in the same directory as go file, and they have read/write permissions**

To add a book mark 'bm' to the 'path', navigate to 'path' and execute go with 'new' option the following command:
```
go new bm
```
This will set a bookmark 'bm' to the present working director (path). To jump to 'path' simply write:
```
go bm
```
Above command will take you to the 'path' and it will also list the contents of the directory by default.

### nts
This script help you create, edit, delete and view notes in bash terminal.

**Make sure to have Notes directory in the same directory as nts file**

To create a new note with 'name' title and 'data' content:
```
nts new -t name -m data
``` 
If no name of message is given nts reads it separately.

To delete a note use:
```
nts rm -t (to delete note with specific title)
nts rm -a (to delete all notes)
```

To edit a note:
```
nts edit -t titleOfTheNote
```

To view contents of a note:
```
nts show -t titleOfTheNote
nts show -l (to view all notes)
nts show -l (to view all notes with last modified date)
```
