# **Git Commands**

## Documentation

- [Git Docs](https://git-scm.com/docs)

## **Configuring Git**

`git config --global user.name "xxxxxx"`

`git config --global user.email "xxxx@xxx.com"`

`git config user.name` or `git config user.email` Check if username or email already exists

`git hash-object <file-name>` Outputs hash `(SHA-1)` for particular file

`git cat-file -p <hash-object>` Outputs file contents

## **SSH Config**

- [Connecting to GitHub with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

## Git I**gnore File**

`.gitignore` Create in root directory

`DS_Store` Will ignore files name `.DS_Store`

`folder_name/` Will ignore an entire directory

`passwords.txt` Will ignore a selected target

`.log` Will ignore any files with the .log extension

## **Committing**

`git --version` Check git version

`git status` Report status in current repository

`git init` Initialise `repo`

`git add` Add files to staging area

`git commit -m "message"` Commit staged files

- Commit early and often
- Keep each commit `atomic` - base unit/base component within a complex system | Each commit should be based on one feature, one thing.
- Convention on Messages recommends Present-Tense, Imperative Style when writing messages.
- Write meaningful but concise commit messages
  `git commit -a -m "message"` Commit and add in same command

`git log` Show who committed to the `repo`

`git log --oneline` Easy to read format

`git commit --amend` Amend last commit

## **Branching**

`git branch` Shows all branches within `repo`

`git branch -v` Detailed view of all branches

`git branch <branch-name>` Creates a branch

`git branch -m <branch-name>` Move or rename

`git branch -c <branch-name>` Copy branch

`git branch -d <branch-name>` Delete branch short

`git-branch --delete <branch-name>`  Delete branch long

`git branch -D <branch-name>` Force delete

`git switch <branch-name>` Switch to another branch

`git switch -c <branch-name>` Create and switch to a new branch

`git checkout <branch-name>` Switch to another branch

`git checkout -b <branch-name>` Create and switch to a new branch

## **Merging**

`git merge <branch-name>` Merge branch to current branch

## **Comparing Files**

`git diff` Compare two files

`git diff HEAD` Changes made since last commit/HEAD

`git diff --staged` Only show staged changes

`git diff --cached` Only cached changes

`git diff <branch-name1>..</branch-name2>` Compare between two branches

## **Stashing**

`git stash list` Displays all stashes

`git stash` Stash all uncommitted changes

`git stash pop` Removes recent commits in stash back

`git apply`

`git apply stash@{n}` Takes changes within stash and applies them

`Changes within stash are not removed`

`git stash drop <stash{n}>` Drops particular stash

## **Detached HEAD**

`git checkout <commit hash>` Check old commits

`git checkout HEAD~n` Reference `n` Commit before HEAD

`git checkout HEAD <file-name>`

`git checkout -- <file-name>` Restore file to previous state before last commit

`git restore <file-name>` Restore file to previous state before last commit

`git restore --source HEAD~1 <file-name>` Restore file to previous state

`git restore --staged <file_name>` Removes file from staging area

`git reset <commit-hash>` Reset the `repo` back to certain commit, changes are kept

`git reset --hard <commit-hash>` Removes changes as well

`git revert <commit-hash>` Creates new commit, undoes and removes old commit

## **Reset Vs Revert**

`git revert` Better when in team that has commit you wish to remove

`git reset` Use when no one in the team has the commit you wish to remove

## **GitHub**

`git clone <url>` Downloads a local copy

`git remote -v` List all remotes in current `repo`

`git remote add upstream <url>` Fork synced with up-to-date

`git remote add <name> <url>` Add a new remote

`git push <remote> <branch>` Push local `repo` to remote branch

`git push origin <local-branch>:<remote-branch>`

Push local branch to remote branch with different name

`git push -u origin <branch-name>`Set the upstream of the branch

`git fetch <remote>`

`git fetch <remote> <branch>`

Fetches the latest changes without merging them into the local repository.

`git pull`

`git pull <remote>`

`git pull <remote> <branch>` Fetch changes and merge

## Rebasing

`git rebase <branch-name>` Rewrite history

Never `Rebase` if feature branch has gone upstream

Never `Rebase` `main` branch

`git rebase -i HEAD~n` Rewrite commit messages

`pick` Use the commit

`reword` Use the commit, but edit the commit message

`edit` Use commit, but stop for amending

`fixup` Use commit contents but meld it into previous commit and discard the commit message `drop` Remove commit

## **Tags**

`Version 2.4.1` - `2` Major Release | `4` Minor Release | `1` Patch release

`git tag -l` List all tags

`git checkout <tag>` Checkout particular commit

`git tag <tag-name>` Create lightweight tag for current commit `HEAD` is pointed too

`git tag -a <tag-name>` Create an annotated tag

`git tag <tag-name> <commit-hash>` Create lightweight tag for previous commit

`git tag -f <tag-name>` Replacing tag with force (move tag to another commit)

`git tag -d <tag-name>` Delete tag

`git push --tags` Push all tags

`git push origin <tag-name>` Push particular tag

## Reflogs

`reflogs` Git keeps a record of when the tip of branches and other references were updated

Only local

They expire - Git cleans out old entries after 90 days

`git reflog show HEAD` Shows all changes to HEAD

`git reflog show HEAD~2` Go back to 2 references (Grand-parent commits)

`git reflog show HEAD@{2}` Go back 2 heads ago

`git dif HEAD@{0} HEAD@{5}` Show the difference between 2 commits

`git reset --hard <commit hash>` Revert/undoing a `rebase`
