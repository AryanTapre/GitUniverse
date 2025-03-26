**Tracked files**
: Files that were in last snapshots, or newly staged file.

**Untracked Files**
: Files that were not part of last snapshot/commit, or not included in staging area before.

![git stages and file states](./git-stages-of-files.png)

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

