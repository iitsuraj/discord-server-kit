# Why Use Git And Github

> 1. Git is the most commonly used version control system.
> 2. Git tracks the changes you make to files, so you have a record of what has been done, and you can revert to specific versions should you ever need to.
> 3. Git also makes collaboration easier, allowing changes by multiple people to all be merged into one source.

# What You Need

> 1. Github account (Create a github account from https://github.com)
> 2. Git cli (Download git cli from https://git-scm.com/downloads and add it path)

# 30+ Git Commands That I Frequently Use

1. git clone

### Create 'blogs' folder and clone the 'pbteja1998/blogs' repo into itCreate 'blogs' folder and clone the 'pbteja1998/blogs' repo into it

    	git clone https://github.com/pbteja1998/blogs.git

### Create `my-blogs` folder and clone the `pbteja1998/blogs` repo into it

    	git clone https://github.com/pbteja1998/blogs.git my-blogs

2. git init

### Initializes the current directory as a git repo

    	git init

3. git add

### Adds the file contents to the index

### Ready to be committed next time you run `git commit`

### By default, Ignores the files present in `.gitignore`

### Add a single file

    	git add README.md

### Add all the files in the current directory

    	git add .

### Also adds the files present in `.gitignore`

    	git add -f .

4. git commit

### Commits/Records the changes to the local repo

    	git commit -m "some message"

### Does not create a new commit

### Adds the changes to the most recent commit

    	git commit --amend

5. git status

### Shows the status of the working tree

    	git status

### Shows the output in short format

    	git status -s

### Shows the branch even in short format

    	git status -sb

6. git log

### Shows the commit logs

    	git log

7. git diff

### Shows the changes between unstaged files and the commits

    	git diff

### Shows the changes between staged(ready-to-be-committed) files and the commits

    	git diff --staged

8. git remote

### Shows all the remotes configured and their remote URL

    	git remote -v

### Adds a remote

### git remote add <_remote-name_> <_remote-url_>

    	git remote add upstream https://github.com/something/blogs.git

### Changes the URL of the remote

    	git remote set-url upstream https://github.com/some-thing/blogs.git

9. git checkout

### Switch to branch

### git checkout <_branch_>

    	git checkout master

### Creates a new branch and switch to that

    	git checkout -b new-feature

### Removes all the unstaged changes in the current directory

    	git checkout .

### Removes all the unstaged changes for a file

    	git checkout -- README.md

10. git push

### Pushes the local changes to the remote to keep it up-to-date

    	git push origin master

### Force push the local changes to the remote

### Usually git will not allow you to push to the remote if the remote has some commits that are not present in local repo

### This will override that check and lets you force push to the remote

### This may cause the remote to lose some commits. So use it carefully.

    	git push -f origin master

### Push and set the remote as upstream

### same as `git push --set-upstream origin feature-branch`

    	git push -u origin feature-branch

### Deletes the branch in the remote

### same as `git push --delete origin new-feature`

    	git push --delete origin new-feature

11. git branch

### Deletes the branch locally

### same as `git branch --delete feature-branch`

    	git branch -d feature-branch

### Force delete a branch even if it's not merged

### same as `git branch --delete --force feature-branch`

    	git branch -D feature-branch

12. git clean

### Removes all the files and directories that are not yet tracked by git

    	git clean -fd

13. git merge

### Merges the <_branch_> to the current branch

### git merge <_branch_>

    	git merge feature-branch

14. git pull

### Fetches the changes from the remote and merge it into local repo

    	git pull origin master

15. git reset

### Removes all the changes to the tracked files that have not yet been committed

    	git reset --hard
