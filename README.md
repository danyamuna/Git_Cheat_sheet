# Git_Cheat_sheet

## Step 1: First-Time Git Setup

```md
$ git config --global user.name "   "
$ git config --global user.email basic@example.com
```
## Step 2 :Your Editor
```md
$ git config --global core.editor "'C:/Program Files/Notepad++/notepad.exe'
-multiInst -notabbar -nosession -noPlugin"
$ git config --global core.editor emacs

```
## Step3 :  default branch name
```md
$ git config --global init.defaultBranch main
```
## Step 4 : Checking Your Settings
```md
$ git config --list
```
## Getting Help
```md
$ git help <verb>
$ git <verb> --help
$ man git-<verb>
```
# Initializing a Repository in an Existing Directory
## Step 5 : Add  & Committing Your Changes
```md
$ git init
$ git add file
$ git commit -m "   "
```
## Checking the Status of Your Files
```md
$ git status
$ git status -s
```
## To see what you’ve changed
```md
$ git diff
```
## Removing Files
```md
$  rm readme.md
$ git rm PROJECTS.md
```
## Moving Files
```md
$ git mv file_from file_to
```
## Viewing the Commit History
```md
$ git log
```





