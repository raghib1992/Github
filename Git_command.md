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
# to check detials of the commit
git show 85f54e99d0ed1a08e1af6cd1e39e12ea6f991068 (commit ID)

# to revert commit - get new commit ID for revert, and previous commit( which we want to revert) also available in logs
git revert 85f54e99d0ed1a08e1af6cd1e39e12ea6f991068 (commit ID)

# to revert the commit but changes will be availble to file
git reset --soft e20802ff79a0f8da778905707eca51f5b980acc6 (commit ID)

# to revert the commit and unstaged the changes
git reset --mixed e20802ff79a0f8da778905707eca51f5b980acc6 (commit ID)

# to revert the commit, unstaged and delete everything from logs
git reset --hard e20802ff79a0f8da778905707eca51f5b980acc6 (commit ID)

# to back to one/x step back commit 
git reset --hard HEAD~1/x

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


# to do stash (not commit) save the changes in stash
git stash

# to check stash
git stash list

# to apply apply changes
git stash apply 0(stash index number)

# to clear stash
git stash clear


#to merger branches
##please be in the branch in which all the chages merges like changes done into shaheen and it will merge into master, before merging exit from shaheen and enter into master
git merge shaheen

# to squash(merge) commit
git rebase -i HEAD~4(no.of commit)


