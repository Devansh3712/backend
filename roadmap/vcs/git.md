git is a version control system that allows one to track changes to files and folders.

# setup and configuration
```bash
# initialize a new git repository
git init
# clone and create a local copy of a remote repository
git clone <url>
# configure global git settings
git config --global <setting> <value>
```

# file operations
```bash
# show working tree status
git status
# add files to the staging area
git add <file(s)>
# remove files from working tree and staging area
git rm <file(s)>
# move or rename a file
git mv <old_file> <new_file>
# commit changes with a message
git commit -m "commit message"
# show differences between working tree and last commit
git diff

# unstage a file, but keep in the working directory
git rm --cached <file>
```

# branching and merging
```bash
# list all branches
git branch
# create a new branch
git branch <name>
# switch to a branch
git checkout <name>
# merge a branch into the current branch
git merge <branch>
# delete a specific branch
git branch -d <name>

# interactive rebase for edit, squash, re-order, or drop commits
git rebase -i
```

# remote repositories
```bash
# fetch from a remote repository
git fetch <name>
# pull changes from a remote repository
git pull <name> <branch>
# push changes to a remote repository
git push <name> <branch>
```

# stashes
```bash
# temporarily save changes in the working tree
git stash save "stash message"
# list all stashes
git stash list
# apply changes from a specific stash
git stash apply <stash>
# remove a specific stash
git stash drop <stash>
# remove all stashes
git stash clear
```

# commit management
```bash
# modify the latest commit
git commit --amend
# create a new commit that undoes changes from a previous commit
git revert <id>
# discard changes and move HEAD to a specific commit
git reset --hard <id>
# show a record of all changes made to the local repository head
git reflog
```

# references
- https://cs.fyi/guide/git-cheatsheet
