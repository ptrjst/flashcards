Git
===

This deck will remind you of all the git goodness you've forgotten.

## Branching and Merging

### Show all local branches

    git branch

### Show all local and remote branches

    git branch -a
    
`-a` is short for `--all`.

### Show only remote branches

    git branch -r

### Create a local branch

    git branch name-of-branch

or if you want to check it out at the same time

    git checkout -b name-of-branch

### Switch to another branch

    git checkout name-of-branch

### Delete a remote branch

    git branch -d name-of-branch
    git push origin :name-of-branch

A slightly more intuitive way of doing that second command:

    git push origin --delete name-of-branch


### When I list all the remote branches, I see things that actually aren't there anymore. What's wrong?

You need to remove the remote tracking branches:

    git remote prune origin
    
## Rewriting history

### Blow away all your work in progress

    git reset --hard origin/name-of-branch

### Undo the last commit

    git reset --hard HEAD~1
    
`HEAD~1` means the commit before head.