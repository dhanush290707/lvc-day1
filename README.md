 # Day 1 Learning Lab

Welcome to **Day 1** of the Learning Version Control series. This repository contains practice exercises, notes, and examples for getting started with Git and GitHub.

## Learning goals

- Understand basic version control concepts
- Create and organize a repository
- Track, stage, and commit changes
- Write clear project documentation

## Getting started

```bash
# Create a new repository
git init

# Copy an existing repository
git clone <repository-url>
cd Day1

# Configure your identity
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# View your Git configuration
git config --list
```

## Exercises

1. Review the project structure.
2. Make a small change to a file.
3. Check the change with `git status`.
4. Commit the change with a descriptive message.

## Basic workflow

```bash
# Show the current branch and working-tree state
git status

# See unstaged changes
git diff

# Stage a specific file or all changed files
git add <file>
git add .

# Unstage a file while keeping its changes
git restore --staged <file>

# Discard changes in a file
git restore <file>

# Save staged changes as a commit
git commit -m "Describe your change"

# Change the most recent commit message or include additional staged changes
git commit --amend -m "Updated commit message"
```

## Viewing history

```bash
# View commit history
git log --oneline

# View a detailed history with a graph
git log --oneline --graph --decorate --all

# Show a commit and its changes
git show <commit>

# Compare two commits, branches, or files
git diff <source> <target>

# Find who last changed each line
git blame <file>
```

## Branches

```bash
# List local branches
git branch

# Create a branch
git branch <branch-name>

# Switch to an existing branch
git switch <branch-name>

# Create and switch to a new branch
git switch -c <branch-name>

# Rename the current branch
git branch -m <new-branch-name>

# Merge another branch into the current branch
git merge <branch-name>

# Delete a merged local branch
git branch -d <branch-name>

# Force-delete a local branch
git branch -D <branch-name>
```

## Remote repositories

```bash
# List configured remote repositories
git remote -v

# Add a remote repository
git remote add origin <repository-url>

# Change a remote repository URL
git remote set-url origin <repository-url>

# Download remote changes without modifying local files
git fetch origin

# Download and merge changes from a remote branch
git pull origin <branch-name>

# Upload a branch and set its upstream branch
git push -u origin <branch-name>

# Upload later commits to the upstream branch
git push

# Delete a remote branch
git push origin --delete <branch-name>
```

## Undoing and recovering changes

```bash
# Temporarily save uncommitted changes
git stash

# List saved stashes
git stash list

# Reapply the latest stash and keep it saved
git stash apply

# Reapply and remove the latest stash
git stash pop

# Remove the latest stash
git stash drop

# Create a new commit that undoes an earlier commit
git revert <commit>

# Move the current branch while keeping changes staged
git reset --soft <commit>

# Move the current branch while keeping changes unstaged
git reset --mixed <commit>

# Move the current branch and discard tracked changes
git reset --hard <commit>
```

Use `git reset --hard` carefully because it permanently removes uncommitted changes.

## Files and tags

```bash
# Rename or move a tracked file
git mv <old-name> <new-name>

# Remove a file from Git and from the working directory
git rm <file>

# Remove a file from Git but keep it locally
git rm --cached <file>

# Create a tag for a release
git tag <tag-name>

# List tags
git tag

# Push a tag to a remote
git push origin <tag-name>

# Push all tags to a remote
git push origin --tags
```

## Cleaning and help

```bash
# Preview untracked files that can be removed
git clean -n

# Remove untracked files
git clean -f

# Get help for a command
git help <command>
```

## Notes

Use this section to record questions, key takeaways, and links discovered during the lesson.

## License

This learning project is provided for educational purposes.
