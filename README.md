# Bash Scripts

## This repo is for useful bash scripts

List of scripts:
1. [go](./bookmark_command/)
2. [nts](./bash_notes/)
3. [autowake](./autowake/)

## Setup
1. Create $HOME/.local/bin/ folder (if it doesn't exist already).
```
mkdir $HOME/.local/bin/
```
2. Make sure the folder is added to $PATH (check .bashrc/.bash_profile/.bash_login/.profile)
```
export PATH="$HOME/.local/bin/:$PATH"
```
3. Clone the repo in $HOME/.local/bin/ (directory for user binaries).

4. Navigate to the cloned repo and add executable permission to commands.
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
This is used when you want to load environment variables, functions, or aliases into your current shell session. It allows you to modify the current shell's environment directly without needing to create a separate subshell.
## Usage

### go
Helps create, delete and view path book marks in terminal.

**Make sure the BM_data.txt and path_data.txt are present in the same directory as go file, and they have read/write permissions**

To add a book mark 'bm' to the 'path', navigate to 'path' and execute go with 'new' option the following command:
```
go new <bookmark>
```
Lists all the book marks along with their respective paths

```
go ls
```
Removes book mark and its path

```
go rm <bookmark>
```
This will set a bookmark 'bm' to the present working director (path). To jump to 'path' simply write:
```
go <bookmark>/<path>
```
Above command will take you to the 'path' and it will also list the contents of the directory by default. To navigate to subfolders use '/<path\>'. Avoid nameing book marks as keywords as good practice, but if you are using keyword as book mark, distinction will be made on the basis of / symbol.

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

### rmt
We have a bunch of computers connected to the server in CC-Lab, this script make wakeonlan easier on those PCs

**Make sure to have ADDR_DATA.txt in the same directory as rmt file**

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

