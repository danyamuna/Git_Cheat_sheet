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
$ git ad -i
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
$ git log -p
$ git log --stat
$ git log --shortstat
$ git log --name-status
$ git log --abbrev-commit
$ git log --relative-date
$ git log --pretty=oneline
$ git log --pretty=format:"%h - %an, %ar : %s"
$ git log --pretty=format:"%h %s" --graph
$ git log --abbrev-commit --p  //

$ git reflog // a log
of where your HEAD and branch references have been for the last few months.
$ git log -g master
Commit Ranges
-“all commits reachable from experiment that aren’t reachable from master.”
$ git log master..new-branch

shows you which side of the range each commit is in
$ git log --left-right master...experiment

      
```
## Limiting Log Output
```md
$ git log -n / n = number

$ git log --author "name"

$ git log --commiter

$ git log -S "function name"

$ git log --grep "name of commit"

$ git log --since =2.week
```
##  Git restore
```md
$ git reset HEAD CONTRIBUTING.md
$ git checkout -- CONTRIBUTING.md
$ git restore --staged CONTRIBUTING.md
$ git restore CONTRIBUTING.md
```

## Git With Remote
```md
$ git clone
$ git remote -v
$ git remote add pp
$ git push pp master
$ git fetch main
$ git pull pp main
$ git remote rename oldname newname      
$ git remote remove newrem
```

## Git show
```md
$ git show ca82a6df
$ git show HEAD@{5}
$ git show master@{yesterday}
Escaping braces in PowerShell
When using PowerShell, braces like { and } are special characters and must be
escaped. You can escape them with a backtick ` or put the commit reference in
quotes:
$ git show HEAD@{0} # will NOT work
$ git show HEAD@`{0`} # OK
$ git show "HEAD@{0}" # OK

see the previous commit
$ git show HEAD^
-On Windows in cmd.exe, ^ is a special character and needs to be treated differently.
You can either double it or put the commit reference in quotes:
$ git show HEAD^ # will NOT work on Windows
$ git show HEAD^^ # OK
$ git show "HEAD^" # OK
- This also refers to the first parent
$ git show HEAD~3
-This can also be written HEAD~~~, which again is the first parent of the first parent of the first parent:
$ git show HEAD~~~

```

## Git Stash And Clean
```md
$ git stash
$ git stash list
$ git stash apply stash@{2}
$ git stash apply --index
$ git stash drop stash@{0}
$ git stash --keep-index
$ git stash -u //untraked file
$ git clean -d -n
$ git clean -d -n -x //delet output file .o
$ git clean -f -d
```

## gpg key / GNU Privacy Guard
```md
$ gpg --gen-key
$ gpg --lis-tkey
$ git config --global user.signingkey 0A46826A
$ git tag -s v1.5 -m 'my signed 1.5 tag
$ git show v1.5
$ git tag -v v1.4
$ git commit -a -S -m 'Signed commit'
$ git log --show-signature -1
$ git log --pretty="format:%h %G? %aN %s"
$ git merge --verify-signatures non-verify
$ git config --local commit.gpgsign true 
```

