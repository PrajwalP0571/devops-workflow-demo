# Git & GitHub Quick Guide

## Basic Git Commands

### Initialize a Git Repository

```bash
git init
```

Creates a new local Git repository.

---

### Check Repository Status

```bash
git status
```

Shows the current state of files (tracked, untracked, modified).

---

### Add Files to Staging Area

```bash
git add filename
```

Add a specific file.

```bash
git add .
```

Add all changed files.

---

### Commit Changes

```bash
git commit -m "Your commit message"
```

Saves staged changes with a meaningful message.

Example:

```bash
git commit -m "Added login feature"
```

---

### Connect to Remote Repository

```bash
git remote add origin <repository-url>
```

Example:

```bash
git remote add origin https://github.com/username/project.git
```

---

### Push Code to GitHub

```bash
git push origin main
```

Uploads local commits to the remote repository.

---

### Pull Latest Changes

```bash
git pull origin main
```

Fetches and merges latest changes from GitHub into your local branch.

---

### Clone a Repository

```bash
git clone <repository-url>
```

Downloads an existing repository to your local machine.

---

## Branching Commands

### Create a New Branch

```bash
git branch branch-name
```

Example:

```bash
git branch feature-auth
```

---

### Switch to Another Branch

```bash
git checkout branch-name
```

Example:

```bash
git checkout feature-auth
```

---

### Create and Switch Branch Together

```bash
git checkout -b branch-name
```

Example:

```bash
git checkout -b feature-dashboard
```

---

### View All Branches

```bash
git branch
```

Shows all local branches.

---

### Delete a Branch

```bash
git branch -d branch-name
```

Deletes a local branch after merging.

---

### Push a Branch to GitHub

```bash
git push origin branch-name
```

Example:

```bash
git push origin feature-auth
```

---

## Merge vs Rebase

### Merge

```bash
git merge branch-name
```

Merge combines changes from one branch into another while preserving the complete branch history.

* Safe and commonly used
* Keeps all commit history visible
* Creates a merge commit

Example:

```bash
git checkout main
git merge feature-auth
```

---

### Rebase

```bash
git rebase branch-name
```

Rebase moves your branch commits on top of another branch, creating a cleaner and linear history.

* Produces a cleaner commit history
* Avoids unnecessary merge commits
* Rewrites commit history

Example:

```bash
git checkout feature-auth
git rebase main
```

---

### Simple Difference

| Merge                     | Rebase                   |
| ------------------------- | ------------------------ |
| Preserves full history    | Creates cleaner history  |
| Adds merge commits        | No extra merge commits   |
| Safer for shared branches | Better for local cleanup |
| Easier to understand      | History looks linear     |

---

## Undoing Changes

### Unstage a File

```bash
git reset filename
```

Removes a file from the staging area.

---

### Discard Local Changes

```bash
git checkout -- filename
```

Restores the file to the last committed state.

---

### Reset Last Commit (Keep Changes)

```bash
git reset --soft HEAD~1
```

Removes the last commit but keeps the changes staged.

---

### Reset Last Commit (Delete Changes)

```bash
git reset --hard HEAD~1
```

Deletes the last commit and all associated changes permanently.

⚠️ Use carefully.

---

### View Commit History

```bash
git log
```

Shows commit history.

---

### Revert a Commit

```bash
git revert commit-id
```

Creates a new commit that undoes a previous commit safely.

Example:

```bash
git revert a1b2c3d
```

---

## Useful Tips

### Fetch Latest Changes Without Merging

```bash
git fetch
```

Downloads changes from remote without applying them.

---

### Check Remote Repository

```bash
git remote -v
```

Displays connected remote repositories.

---

### Rename Current Branch

```bash
git branch -M main
```

Renames the current branch to `main`.

---

# Conclusion

Git helps track changes, collaborate with teams, and manage project history efficiently. Understanding commits, branches, merges, and undo operations is essential for every developer.

