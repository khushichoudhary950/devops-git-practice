## Difference Between git fetch and git pull

| git fetch | git pull 
|------------|-----------|
| Downloads the latest changes from the remote repository. | Downloads the latest changes and merges them into the current branch. |
| Does not modify your working files. | Updates your working files automatically. |
| Safe for checking new changes before merging. | Best when you want your local branch updated immediately. |

### Commands

```bash
git fetch
```

Downloads new commits from GitHub but does not merge them.

```bash
git pull
```

Downloads new commits and immediately merges them into the current branch.

### Relationship

```text
git pull
      │
      ▼
git fetch
      +
git merge
```

So,

git pull = git fetch + git mergeIn this file we practise all git commands

git init 
git add
git commit
git status


# Git Commands Guide

## Basic Git Commands

### Initialize a Git Repository
```bash
git init
```
**Purpose:** Initializes a new Git repository in the current directory.

---

### Check Repository Status
```bash
git status
```
**Purpose:** Displays the current state of the repository, including modified, staged, and untracked files.

---

### Stage a Specific File
```bash
git add <file-name>
```
**Example:**
```bash
git add notes.txt
```
**Purpose:** Stages a specific file for the next commit.

---

### Stage All Files
```bash
git add .
```
**Purpose:** Stages all modified and new files.

---

### Commit Changes
```bash
git commit -m "Commit Message"
```
**Example:**
```bash
git commit -m "Added Day 23 notes"
```
**Purpose:** Saves a snapshot of the staged changes.

---

### View Commit History
```bash
git log
```
**Purpose:** Displays detailed commit history.

---

### View Commit History (Short)
```bash
git log --oneline
```
**Purpose:** Displays commit history in a concise format.

---

## Branching Commands

### List All Branches
```bash
git branch
```
**Purpose:** Displays all local branches. The branch marked with `*` is the current branch.

---

### Create a New Branch
```bash
git branch feature-1
```
**Purpose:** Creates a new branch without switching to it.

---

### Switch to an Existing Branch
```bash
git switch feature-1
```
**Purpose:** Switches to the specified branch.

**Older Alternative:**
```bash
git checkout feature-1
```

---

### Create and Switch to a New Branch
```bash
git switch -c feature-2
```
**Purpose:** Creates a new branch and immediately switches to it.

**Older Alternative:**
```bash
git checkout -b feature-2
```

---

### Delete a Merged Branch
```bash
git branch -d feature-2
```
**Purpose:** Deletes a branch that has already been merged.

---

### Force Delete a Branch
```bash
git branch -D feature-2
```
**Purpose:** Deletes a branch even if it has not been merged.

---

## Branch Switching

### Switch Back to Main Branch
```bash
git switch main
```
**Purpose:** Returns to the `main` branch.

---

### Verify Current Branch
```bash
git branch
```
**Purpose:** Displays all branches and highlights the current branch.

---

## Difference Between `git switch` and `git checkout`

| `git switch` | `git checkout` |
|--------------|----------------|
| Used only for switching branches | Used for switching branches, restoring files, and creating branches |
| Easier for beginners | Older command with multiple purposes |
| Introduced in newer Git versions | Available in all Git versions |

---

# Git Branch Workflow

```text
Start on main
      │
      ▼
Create Branch
git branch feature-1
      │
      ▼
Switch Branch
git switch feature-1
      │
      ▼
Make Changes
      │
      ▼
git add .
      │
      ▼
git commit -m "Added new feature"
      │
      ▼
Switch Back
git switch main
      │
      ▼
Delete Branch (if no longer needed)
git branch -d feature-1
```

---

# Quick Cheat Sheet

| Command | Description |
|---------|-------------|
| `git branch` | List all local branches |
| `git branch <branch-name>` | Create a new branch |
| `git switch <branch-name>` | Switch to a branch |
| `git switch -c <branch-name>` | Create and switch to a new branch |
| `git checkout <branch-name>` | Switch branches (older command) |
| `git checkout -b <branch-name>` | Create and switch (older command) |
| `git branch -d <branch-name>` | Delete a merged branch |
| `git branch -D <branch-name>` | Force delete a branch |
| `git status` | Show repository status |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Commit staged changes |
| `git log --oneline` | View concise commit history | 
