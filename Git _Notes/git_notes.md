# GIT

## Why We Use Version Control Systems
- **Purpose**: For collaboration, storing versions, tracking changes, and creating backups.
- **Issues Without Version Control**:
  - All changes made to files are permanent and cannot be reverted.
  - No record of what was done and by whom.
  - Downtime due to faulty code can result in significant losses.

## What is Version Control?
- A system that tracks changes made to files or sets of files.
- Allows multiple users to manage multiple versions of the same information.
- Acts as a snapshot of your project over time.

---

## Types of Version Control Systems

### 1. Local Version Control (LVC)
- **Description**: Keeps a version database on the local computer.
- **Issue**: Multiple people working on the same project in parallel causes conflicts.
- **Solution**: Centralized Version Control System (CVCS).

### 2. Centralized Version Control System (CVCS)
- **Description**: Maintains a central repository where all versioned files are stored. Users can check in and out files from their computers.
- **Issue**: If the central server fails, the entire system goes down.
- **Solution**: Distributed Version Control System (DVCS).

### 3. Distributed Version Control System (DVCS)
- **Description**: Stores the version database on every user's local system as well as on a remote server.
- **Advantages**:
  - Users can manipulate files locally and then push changes to the remote server.
  - If the central server fails, any client server can restore the data.

---

## What is Git?
- **Definition**: Git is an open-source Distributed Version Control System (DVCS).
- **Key Features**:
  - Records changes to files.
  - Emphasizes speed, data integrity, and distributed, non-linear workflows.

---

## Git Workflow
![preview](./img/basic-remote-workflow.png)


### 1. Working Space
- The user’s active directory where files are created or modified.
- Git tracks changes in this space compared to the local repository.

### 2. Staging Area
- A place where modified files are marked for commit.

### 3. Local Repository
- A user’s copy of the version database.
- All files are accessed and modified locally before being pushed to the remote repository.

### 4. remote repository

 - A Git remote repository is a version-controlled repository hosted on a remote server. It serves as a centralized location where team members can push, pull, and collaborate on code.
---

## Git Commands

### Repository Setup
- **`git init`**: Creates an empty repository in a specific folder.
  ```bash
  git init /path/to/folder
git clone <repository_url>: Copies a remote repository to the local machine. Essential for setting up local development environments or build servers.

git pull: Fetches changes from a remote repository and merges them into the current branch. Keeps local branches up-to-date.

git add <file(s)>: Stages changes for commit.

git commit -m "<message>": Records staged changes with a descriptive message. Crucial for tracking changes and collaboration.

git push: Uploads local commits to a remote repository

git branch: Lists, creates, or deletes branches. Used for managing feature development, releases, and hotfixes.

git checkout <branch_name>: Switches to a specified branch.

git merge <branch_name>: Merges changes from one branch into another (e.g., merging a feature branch into the main branch).

git checkout -b <new_branch_name>: Creates a new branch and switches to it.

git tag <tag_name>: Creates a tag to mark a specific release version. Important for tracking releases and rollbacks.

git log: Displays commit history, useful for tracking changes and debugging.

git diff: Shows differences between files, commits, or branches. Helps in understanding changes before merging.

git status: Shows the status of the working directory and staging area.

git fetch: Downloads objects and refs from another repository but doesn't merge them. Useful for CI systems to check for new changes without disrupting the current workspace.

git remote: Manages remote repositories. Used to set up connections to remote repositories for CI/CD pipelines.

git stash: Temporarily saves changes that are not ready to be committed. Useful for switching branches without committing incomplete work.   

git reset: Resets the current branch to a specified state. Can be used for undoing commits or changes

git squash is a way to combine multiple commits into a single commit.

git cherry-pick is a powerful Git command that allows you to select specific commits from one branch and apply them to another branch.

git log is a powerful command that displays the commit history of a Git repository.

 git rebase -i <base>
 Interactively rebase current branch onto <base>. Launches editor to enter commands for how each commit will be transferred to the new base.

 git config --global user.name <name> Define the author name to be used for all commits by the current user

 git revert <commit> Create new commit that undoes all of the changes made in <commit>, then apply it to the current branch.

git reset <file> Remove <file> from the staging area, but leave the working directory unchanged. This unstages a file without overwriting any changes

 git reflog Show a log of changes to the local repository’s HEAD. Add --relative-date flag to show date info or --all to how all refs


Branching Strategy:

Base (Main): The major snapshot of the project.

Dev: Development branch.

QA/Test: For testing and quality assurance.

Release: A branch for release preparation.

Feature: Separate branches for new features.

Hotfix: Used for fixing issues in production.

Pull Request (PR): A request to merge changes from one branch into another.

Clone Command: Creates a copy of an existing remote repository inside the local repository.

Staging Area: Temporary space to prepare files for commit.







