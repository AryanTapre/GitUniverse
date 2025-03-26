**Tracked files**
: Files that were in last snapshots, or newly staged file.

**Untracked Files**
: Files that were not part of last snapshot/commit, or not included in staging area before.

![git stages and file states](./resources/git-stages-of-files.png)

---

#### :new: :wrench: Git setup -- Never used before on local machine


> Configure user details (*username* and *email*).
> 
- git config --global user.name <user_name> 
- git config --global user.email <user_email>

> Setting up default text editor
> 
- git config --global core.editor <editor_name>

> Setting up default branch to **main**
> 
- git config --global init.defaultBranch main

---

#### Must know commands as developer

> Check current state of repository
>
- git status

> Add files to staging area
>
- git add <file_name> (*adding single file*)
- git add . (*adding all filesx`*)

> Unstage files from staging area / index
> 
- git restore --staged <file_name>

> Display repo status in short
> 
- git status --short

> shows changes made to file who not in staging area
> 
- git diff

> shows changes made to file who in staging area
> 
- git diff --staged

> Commit files currently staged
>
- git commit -m "<commit_message>"
- git commit (*opens default editor to type commit msg

> Skip staging area --direct commit
> 
- git commit -a -m "<commit_message>"

> Remove files from git control, deleting it
>: does auto stage and commit for us
- git rm <file_name> (**)

> Renaming a file
>
- git mv <old_file_name> <new_file_name>

---

#### Working with *dotgitignore* files

- :warning: <ins>**what git does**</ins>: If file to ignore by git is already committed / tracked, even after adding it's name to .gitignore file git refuses to ignore it.

- Firstly add <file_name> in .gitignore file

- untrack file using below command
    - git rm --cached <file_name>

- commit the changes


---

#### Let's see some git history commands

> List all commits uptill now
>
- git log

> List all commits with file content differences
>
- git log --patch

> List commits customize to display
>
- git log <number> (*git log 2 : will display last two commits*)


> Show commits log in various formaots
> 
- git log --pretty = fuller/full/oneline/short

> Display log since particular date (yyyy-mm-dd)
> 
- git log --since="yyyy-mm-dd"

> Display log untill particular date (yyyy-mm-dd)
> 
- git log --untill="yyyy-mm-dd"

> Display log before particular date (yyyy-mm-dd)
> 
- git log --before="yyyy-mm-dd"

> Display log after particular date (yyyy-mm-dd)
> 
- git log --after="yyyy-mm-dd"


---
#### Git undoing changes

> To rewrite the commit
>: If you want to redo the commit, make additional changes you forget stage them and commit again use --amend option 

*As an example, if you commit and then realize you forgot to stage the changes in a file you wanted to add to this commit, you can do something like this:*

-  git commit -m <Initial commit>
   git add forgotten_file 
   git commit --amend 

> Unstage files, effectively removing them from staging area
>
- git restore --staged <file_name>

> Undo content of any file tracked by git
>: Discard local changes and revert back to last committed state 
- git restore <file_name>

> Reverse changes of the commit
> 
- git revert <commit_hash>




