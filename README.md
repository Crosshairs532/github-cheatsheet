# github-cheatsheet
Most common github commands every developer use.

# 1. `Git Configure :`
> set username, set email used for creating github account
> ```git
> git config --global user.name [your user name]
> git config --global user.email [your email address]
> ```
>#### To see all the configs
> ```git
> git config --global --list: all the global  configurations will be shown here
> git config --local --list: all the local configurations will be shown here. This works only inside a repository
> git config --system --list: all the local configurations will be shown here. This works only inside a repository
> ```
>####  To unset a configuration
> you can do this for local, global and system as well
> ```git
> git config --global --unset user.name
> git config --global --unset user.email
> ```
# 2. `Git Basic Commands`
> ```git
> git init
> ```
> ```git
> git add [. , -A, "file name"]
> git commit -m "any meassge"
> git commit -am "any message" // add + commit message
> git commit --amend // append new texts to prev commit. 
> ```
> check status 
> ```git
> git status
> ```
> The file I want to restore. basically, it will go back to the previous stage from staging
> ```git
> git restore "file name"
> ```
> To Check Difference between the files that has been commited
> ```git
> git diff
> ```
> To check all the commits(commit history)
> ```git
> git log
> git log --oneline
> ```
> To reset commit
> ```git
> git reset --soft HEAD^
> git reset HEAD^
> git reset --hard HEAD^
> ```
> Go back to the specific commit address
> ```git
> git checkout "commit id" // jump to checkpoint
> git checkout "branch name" // jump to different branch
> git checkout -b "branch name" // create and jump to new branch
> git switch 'branch name' // jump to different branch
> git switch -c 'branch name' // create and jump to new branch
> git revert
> git reset
> git clean
> git rm
> ```
>  go to the recent commit
> ```git
> git checkout master
> ```
> check the history of a specific commit
> ```git
> git show
> git show HEAD
> git show "commit id"
# 3. Git Aliases
> alias."some name" "For which git command it want the alias for"
> ```git
> git config --global alias.ci "commit"
> ```
