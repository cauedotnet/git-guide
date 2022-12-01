## Simple guide of Git Commands

# Basic Everyday Use

```
# Add all files to Git
$ git add .

# Commit (to local repository)
$ git commit -m "message"

# Push (send to remote repository)
$ git push

# Show files added to the index, files with changes, and untracked files
$ git status

# Diff - Show what changes you made
$ git diff
```

# Install

Download for [OSX](https://git-scm.com/download/mac), [Windows](https://gitforwindows.org/) or [Linux](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

# Setup Credentials

```
# Global
git config --global user.name "Caue.A"
git config --global user.email "caue.a@myemail.com"

# Or Local 
git config user.name "Caue A"
git config user.email "caue.a@myemail.com"
```

# Setup Repo

```
# Clone a Repo from a Url
git clone <url>

# Or Create an empty GIT repository
git init
```

# Adding / Deleting Files

```
# Add all files to Git
git add .

# Add specific files to Git
git add <file1> <file2>

# Add a folder to Git
git add <foldername>

# Remove File from Git
git rm <file1> <file2>
```

# Commit

```
# Commit with message
git commit <file> -m "Message"

# Commit to All Tracked Files
git commit -a -m "Message"

# Reverts changes you made in a file
git checkout -- <filename>
```

# Status and Changes

```
# Show files added to the index, files with changes, and untracked files
git status

# Show unstaged changes made since your last commit
git diff

# Show changes staged for commit
git diff --cached

# Show changes made since last commit
git diff HEAD

# Show changes between branches
git diff <source_branch> <target_branch>

# Tagging (recommended for software releases)
git tag <version> <first-10-chars-of-commit-id> (ex: git tag 1.0.0 c053020dae)
```

# History
```
# All Git Commits (Reverse Chronological Order)
git log

# All Git Commits with Diffs
git log -p

# Git Log with Graph
git log --all --decorate --oneline --graph

```

## Branching

```
Creates a new branch named "my_new_feature" and switch to it
git checkout -b feature_x

# Creates a new branch based on a existing one, and switch
git checkout -b <newbranch> <existingbranch>

# Switch to another branch
git checkout <branchname> (ex: git checkout master)

# Merge contents of <newbranch> to <oldbranch> * The Git merge --no-ff command merges the specified branch into the command in the current branch and ensures performing a merge commit even when it is a fast-forward merge.
git merge --no-ff <newbranch>

# Send to remote repo (otherwise it stills local)
git push origin <branch>

# Delete the branch
git branch -d my_new_feature
```