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
> restore
> ```git
> // The file I want to restore. basically, it will go back to the previous stage from staging
> git restore "file name"
> git restore --staged 'file name' // discard changes from the staging area 
> git restore --staged --wroktree . //
> git restore . // discard changes from the working directory
> git restore --stages --worktree . // discard changes from the working directory + staging
> git restore --source='commit' . //
> git restore --source=HEAD~[1,2,3] // restore the filed in a particular commit from the head. 
> ```
> reset
> ```git
> // suppose i commited some changes. now i want to have changed my mind and i want to reset the commit
> git reset // reset from staged to unstaged. 
> git reset --soft HEAD~[1,2....] // undo the commit =>  currently on staging -> then we can commit. 
> git reset --mixed HEAD~[1,2...] // undo the commit +  unstage // need to `add .` to go to staging -> then we can commit. 
> git reset HEAD^
> git reset --hard HEAD~[1,2....] //undo the commit  + staging + delete the changes from the local file. 
> ```
> rebase
> ```git
> A -> B main
> \ 
>   C - D feature
>
> A -> B -> c-> D linear
>
> from main
> git rebase feature 
>
> 
> ```
> 
> To Check Difference between the files that has been commited
> ```git
> git diff
> ```
> To check all the commits(commit history)
> ```git
> git log
> git log --oneline
> git log -p // see code changes on commit
> git log --stat // details of changes on commit
> git log --oneline --all // see all commits from all branches
> git log --oneline --all --graph // graph of all commits from all branches
> git --no-pager log -n 'any number' // any number of commit we want to see
> ```
> Go back to the specific commit address
> ```git
> git checkout "commit id" // jump to checkpoint
> git checkout "branch name" // jump to different branch
> git checkout -b "branch name" // create and jump to new branch
> git switch 'branch name' // jump to different branch
> git switch -c 'branch name' // create and jump to new branch
> git revert // undo a commit and create a new commit.
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
> git stash --keep-index // stash only the unstracked files
> git stash --include-untracked // stash the untracked files also 
> 
> ```
> fetch & pull
> ```git
>  git branch -r // see all the branches of the remote repo
>
> git pull = git fetch + git merge
> git pull --ff-only
> git pull --ff // download  + basic merge 
> git pull --rebase
> 
> ```
> Branching & Mergin
> ```git
> git branch // see all the branch 
> git branch <name> // creates a new branch
> git branch <name> <sha id> // creates a new branch after specific commit id(sha id)
> git checkout <name> // move to another branch
> git checkout -b <name> // create branch and move to it
> git branch -d <name> // delete a specific branch
> git branch -D <branch > // delete a specific branch 
> git merge <branch> // 
> ```
# 3. Git Aliases
> alias."some name" "For which git command it want the alias for"
> ```git
> git config --global alias.ci "commit"
> ```
