****************************
# ********** Git *************
****************************
# Git Configure
## Install git
## to check git version
```
git --version
```
## to configure username on git
```
git config --global user.name "raghib1992"
```

## to configure your email
```
git config --global user.email "raghib.npti@gmail.com"
```

## to check git config
```
git config --list --show-origin
```
***************************************************
# Create Repo
## command to create git repo
## go into the folder where you want to create repo
```
git init
```
## to check status of your local repository
```
git status
```

## to staged all changes
```
git add filename
git add .  ## (to stage all the files in the repo in which changes are made)
git add *.txt (to satge file with .txt)
```
## to commit changes in the local repository
```
git commit -m "add messages here to get description about commit"
```
## to commit all unstage changes, or add commit in one command
```
git commit -a -m "message"
```
## To edit commit message in VS code
```
git config --global core.editor "code --wait"
```

## to check all the previous commit on our local repository
```
git log
```
## to check detials of the commit
```
git show 85f54e99d0ed1a08e1af6cd1e39e12ea6f991068 (commit ID)
```
## to amend the last commit message or amend the last commit
```
git commit --amend
```
************************************************************
# Branches
## Head
### Head tell us the reference, where we are, the current branch and commit
## To get the list of branch
```
git branch
```
## Create new branch
```
git branch <branch name>
```
## To switch to different branch
```
git switch <branch name>
git checkout <branch name>
```
## To create new branch and switch into it
```
git switch -c <branch name>
git checkout -b <branch name>
```
## To delete branch
```
git branch -d <branch name>
git bracnch -D <branch name>
```
## To rename the branch
```
git branch -m <new branch name>
```
*************************************
# Merging Branches
## Move to receving branch
## fast forward merge
```
git merge <branch name>
```
## Generating Merge without conflict
```
git merge <branch name> # commit message
```
## Generating Merge with conflict
```
git merge <branch name>
```
### edit the conflict file
```
git add <file name>
git commit -m "<message>"
```
*****************************************
# Difference
## To check the changes done for unstage changes
```
git diff
```
## list all changes in working tree since your last commit
```
git diff HEAD
git diff HEAD <filename>
```
## list all the changes of stage and last commit
```
git diff --staged
git diff --staged <filename>
git diff --cached
```
## comapare difference in two branches
```
git diff branch1..branch2
```
## comparing across commit
```
git diff <commit1>..<commit2>
```
****************************************
# Stash
## TO hide or remeber the changes without commit
```
git stash
git stash save
```
## to get recent stash to same or different branch, it remove the stash
```
git stash pop
```
## to apply stash to multiple branches, it keep the stash
```
git stash apply
```
## stashing multiple time and to get the list of stash
```
git stash list
```
## to apply a particular stash from the list of stash
```
git stash apply stash@{2}
```
## to delete to remove stash
```
git stash drop <stagh id>
git stash clear
```
*****************************************
# Checkout
## to go into "detached head" mode: You can look around and make experimental changes and commit them, and you can discard any commits you make in this state without impacting nay branches by switiching back to a branch.
```
git checkout <commit hash>
```
## back to head attach
```
git checkout master
git switch master
```
## to go back to commit with counting the commit, last commit is 1, second last is 2 and so on
```
git checkout HEAD~4
```
## undo changes before staged
```
git checkout HEAD <filename>
git checkout -- <filename>
```
*****************************************
# Restore
## undo changes before staged
```
git restore <filename>
```
## undo the changes of a any to back to desire commit
```
git restore --source HEAD~4 <filename>
```
## to remove file from from stage back before commit
```
git restore --staged <filename>
```
*****************************************
# Reset
## To undo commit and unstagged the changes, but keep the changes
```
git reset <commit hash>
```
## to revert the commit and unstaged the changes
```
git reset --mixed <commit hash>
```
## To undo commit and delete the changes
```
git reset --hard <commit hash>
git reset --hard HEAD~4
```
****************************************
# Revert
## Undo changes but make new commit for the same
```
git revert <commit hash>
```
***************************************
# ********** GitPush*****************
***************************************
# Cloning
## To get remote repo on your local achine
```
git clone <repo url>
```
**************************************
# Setup SSh key or public token
## Ref ssh key
```
https://docs.github.com/en/enterprise-server@3.0/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account
```
## Ref for Personal Access Token
```
https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
```
***************************************
# Send local repo to github first time
## Create new emty repo on github
## To view an existing remote, list of remotes
```
git remote -v
```
## Adding a new new remote to your local repo
```
git remote add <name> <url>
git remote add origin <url>
```
## Push the changes to remote
```
git push <remote> <branch>
git push origin master
```
****************************************
## Rename remote repo
```
git remote rename <old> <new>
git remote remove <name>
```
## push from different local branch to different remote branch
```
git push origin <local branch>:<remote branch>
```
## to set upstream of local and remote
```
git push -u origin <branch name>
git push -u origin <local-branch>:<remote brnach>
```
*******************************************
# Remote Tracking Branch
## to see the list all remote branch
```
git branch -r 
```
## to check the commit difference between remote brnach and the local brnack
##### check the second line of the output of the command
```
git status
```
## to checkout remote pointer branch 
```
git checkout origin/master
```
## switch to remote branch not available locally
```
git switch <remote branch>
git checkout --track origin/puppies
```
*********************************************
# Fetch
## get changes from remote repo but not integrated with my working files
```
git fetch <remote>
git fetch origin
git fetch <remote> <branch>
```
********************************************
# Pull
## Get the changes from the remote branch and merge it to locally
```
git pull <remote> <branch>
git pull
```
*******************************************
