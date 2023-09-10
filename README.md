---
title: GitBash-Cheatsheet
description: Git Bash all necessary commands for using Github
---
# GITHUB COMMANDS SHEET


## SETUP



set a name that is identifable for credit when review version history

```bash
  git config --global user.name "[firstname lastname]"
```
set an email address that will be associated with each hustory maker

```bash
  git config --global user.email "[valid-email]"
```
set automatic command line coloring for Git for easy reviewing

```bash
  git config --global color.ui auto
```
Get global config

```bash
  git config --global --list
```

## SETUP & INIT
 initialize an existing directory as a Git repository

```bash
  git clone https://link-to-project
```

 retrieve an entire repository from a hosted location via URL

```bash
  git clone [url

```
## STAGE & SNAPSHOT

show modified files in working directory , staged for your next commit

```bash
  git status
```
Clone private repository
```bash
  git clone ssh://git@github.com/[username]/[repository-name].git
```
Add all new and changed files to the staging area

```bash
  git add -A
```
Remove a file (or folder)

```bash
  git rm -r[file-name.txt]
```
show modified files in working directory , staged for your next commit

```bash
  git status
```

add a file as it looks now to your next commit (stage)

```bash
  git add [file] 
```
unstage a file while retaining the changes in the working directory

```bash
  git reset [file] 
```
diff of what is changed but not staged

```bash
  git diff 
```
diff of what is staged but not committed

```bash
  git diff --staged
```
commit your staged content as a new commit snapshot

```bash
  git commit -m "[descriptive message]" 
```

## BRANCH & MERGE 

 list your branches. a * will appear next to the currently active branch

```bash
  git branch 
```
Push a branch to your remote repository
```bash
  git push origin [branch name]
```
Push changes to remote repository (and remember the branch)

```bash
  git push -u origin [branch name]
```
Delete a remote branch

```bash
  git push origin --delete [branch name]
```

Update local repository to the newest commit

```bash
  git pull
```
Pull changes from remote repository

```bash
  git pull origin [branch name]
```
Add a remote repository

```bash
  git remote add origin ssh://git@github.com/[username]/[repository-name].git 
```
Set a repository's origin branch to SSH

```bash
  git remote set-url origin ssh://git@github.com/[username]/[repository-name].git
```
Update local repository to the newest commit

```bash
  git pull
```
switch to another branch and check it out into your current working directory

```bash
  git checkout 
```
merge the specified branch's history into the current one

```bash
  git merge [branch] 
```
show all commits in the current branch history

```bash
  git log 
```
View changes (detailed)

```bash
  git log --summary
```
Switch to a branch

```bash
  git checkout [branch name
```
Switch to the branch last checked out

```bash
  git checkout
```

Discard changes to a file

```bash
  git checkout -- [file-name.txt]
```
List all branches (local and remote)

```bash
  git branch -a
```
Delete a branch

```bash
  git branch -d [branch name]
```
Delete a branch forcefully

```bash
  git branch -D [branch name] 
```
## INSPECT & COMPARE
show the commits on branchA that is not in branchB

```bash
  git log branchB..branchA
```
show any object in Git in human-readable format

```bash
  git show [SHA]
```
## TRACKING PATH CHANGES
delete the file from project and stage the removal for commit

```bash
  git rm[file] 
```
change an existing file path and stage the move

```bash
  git mv [existing-path] [new-path]
```
Show all commit logs with indication of any paths that moved

```bash
  git log --stat -M
```
## SHARE & UPDATE
add a URL as an alias

```bash
  |git remote add [alias] [url] 
```
fetch down all the branches from that Git remote
```bash
  git fetch [alias]
```
merge a remote branch into your current branch to bring it up to date

```bash
  git merge [alias]/[branch] 
```

## RERWITE HISTORY
 apply any commmits of currents branch ahead of specified one

```bash
  git rebase [branch]
```
clear staging area, rewrite working tree from specified commit

```bash
  git reset --hard [commit]
```
## TEMPORARY COMMITS
save modified and staged changes

```bash
  git stash
```
list stack-order of stashed file changes

```bash
  git stash list
```
 write working from top of stash stack

```bash
  git stash drop
```
discard the changes from top of stash stack

```bash
  git reset --hard [commit]
```
Remove all stashed entries

```bash
  git stash clear
```
discard the changes from top of stash stack

```bash
  git reset --hard [commit]
```
## Download the official CheatSheet From official Github itself:
[Git_Cheatsheet](https://github.com/DevJSter/GitBasicCommands/files/12446572/git-cheat-sheet-education.pdf)

## However I'll be providing you official docs of sepcific command line commands of Git and Github

1. You need to ensure you have Git installed in your system: You can install git [here](https://git-scm.com/downloads). 
2. To learn more about what is a fork in Github, refer to this [doc on forking](https://docs.github.com/en/get-started/quickstart/fork-a-repo).

3. To learn more about what is a clone in Github, refer to this [doc on cloning](https://docs.github.com/en/get-started/quickstart/fork-a-repo#cloning-your-forked-repository).

4. Learn more about git branching [here](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)

5. Learn more about how to create a new branch in git [here](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Mergin

6. Learn about syncing a fork [here](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/syncing-a-fork)

7. Learn about how to configure a remote for a fork [here](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/configuring-a-remote-for-a-fork)

8. Learn about creating a Pull Request [here](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)

9. Learn about creating a Pull Request from a forked repository [here](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork)

10. Learn about creating a Pull Request from a branch [here](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request#creating-the-pull-request)

11. Learn about creating a Pull Request from a forked repository and branch [here](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork#creating-the-pull-request)

12. Learn about how to rebase your commits by using ``git log --oneline`` [Git Rebase](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)

13.Learn more abou the squashing after rebasing the commits when you used ``git rebase -i Head~(how many9 commits you wamma squash)`` [Git Squash](https://www.freecodecamp.org/news/git-squash-explained/)

14.Learn more about Merging the commits to main repos [Git Merge](https://www.atlassian.com/git/tutorials/using-branches/git-merge)


[Official_Docuementation Link and pdf of it](https://git-scm.com/book/en/v2)
