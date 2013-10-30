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

### Set the remote for a branch

	git branch --set-upstream-to=origin name-of-branch

### Add a remote to the `.git/config` file

	[remote "somewhere"]
		url = http://username@host.name.com/scm/my-app.git
		fetch = +refs/heads/*:refs/remotes/somewhere/*

### Show all commits in a branch that aren't in master

	git log master..name-of-branch
	
or if you want to be fancy:

	git log --pretty=short --graph --all master..name-of-branch

### List all branches already merged into master

	git branch --all --merged master

### List all branches not merged into master

	git branch --all --no-merged master
	
### Show all commits made just to branch, excluding everything merged in from master re-syncs

	git log --first-parent	

### When I list all the remote branches, I see things that actually aren't there anymore. What's wrong?

You need to remove the remote tracking branches:

    git remote prune origin

### Search all commit messages for a word

	$ git log --oneline | grep bump
	248a958 version bump to 3.0.7
	816ed01 version bump 3.0.6

## Rewriting history

### Blow away all your work in progress

    git reset --hard origin/name-of-branch

### Undo the last commit

    git reset --hard HEAD~1
    
`HEAD~1` means the commit before head.

### Squash many commits into one

Let's say you want the last five commits to be one. You'd do:

	git rebase -i HEAD~5

## Stats

### Total project commit count

	git rev-list master --count

### Total commits by each person

	git shortlog -sn

### Lists all commits made by a person

	git log --author="<author name>" --oneline --shortstat

## Resources

http://blog.thefrontiergroup.com.au/2012/07/git-basics-cleaning-up-excess-branches/