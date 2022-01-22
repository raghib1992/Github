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
git diff --cache
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
git stash savez
```
## to apply stash to same or different branch
```
git stash pop
```
## to apply stash to multiple branches
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
## to go into "detached head" mode
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



# to push your repository from local to remote (github account)
git push origin master(branch)

# to check remote repo where we can puch our commit
git remote

# to pull all the changes made in the remote serve to the local repo
git pull origin(remote location) master(branch)

# to show the list of branch
git branch


# to create new branch
git branch rashid(new_branch_name)

# to exit current branch and enter into new branch
git checkout rashid((new_branch_name)
## while doing git branch...current branch will be highlighted with * and green colour

# to create a branch and enter into that brach i.e. combine abouve two command
git checkout -b shaheen(new_branch_name)    #new branch created and enter into same

# to push commit which has been done by branch which unknow to remote server
git push --set-upstream origin shaheen(new branch unknown to remote)

# to squash(merge) commit
git rebase -i HEAD~4(no.of commit)


