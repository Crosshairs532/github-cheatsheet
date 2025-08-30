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
>```
> stash
> ```git
> // i am working in a directory
> // i want to swtich to a new branch
> // but i dont want modified file to go to the new branch
> // We use git stash
>
> git stash // save the current modifiel files to somewhere. 
> git stash list // see all the stashed list.
> git stash pop // bring back what we saved
> git stash apply 'select the partcular stash from the list' // stash wont get popped + we can use the stashed files
> git stash drop 'select the partcular stash from the list' // drop stash from the list
> git stash clear // delete all the stashes
> git stash -- 'partical file' // we can stash single file
> git stash -m 'any message' -- 'particular file' // we can also send messages
> git stash show 'stage name'
> git stash show -p 'stage name'
>  git stash --keep-index // stash only the unstracked files
> git stash --include-untracked // stash the untracked files also 
> 
> ```
# 3. Git Aliases
> alias."some name" "For which git command it want the alias for"
> ```git
> git config --global alias.ci "commit"
> ```
