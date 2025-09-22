# Git Configuration Commands 
## User Information
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
````

## View Current Config

```bash
git config --list
git config user.name
git config user.email
```
---

# Git Commands to Push Codes 


## 1. Initialize Git (if not already a repo)
```bash
git init
````
## 2. Stage Changes

```bash
git add .
```
## 3. Commit Changes

```bash
git commit -m "Initial commit"
```
## 3. Add Remote Repository

```bash
git remote add origin https://github.com/username/repository.git
```


## 5. Push to GitHub

```bash
git branch -M main
git push -u origin main
```

## 6. For Later Updates

```bash
git add .
git commit -m "Update message"
git push
```
---


# Git Commands to Pull Code

## 1. Clone Repository (first time only)
```bash
git clone https://github.com/username/repository.git
````

## 2. Pull Latest Changes

```bash
git pull origin main
```

## 3. If You Are on the Same Branch

```bash
git pull
```
---

# Git Conflicts and Merges

## 1. Merging a Branch
```bash
git checkout main
git merge feature-branch
````

## 2. Conflict Detected

* Git will mark conflicts in the files.
* Look for lines with:

  ```
  <<<<<<< HEAD
  your changes
  =======
  incoming changes
  >>>>>>> branch-name
  ```

## 3. Resolve Conflict

* Manually edit the file(s) to keep the correct changes.
* Remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).

## 4. Stage Resolved Files

```bash
git add conflicted-file.txt
```

## 5. Complete the Merge

```bash
git commit
```

## 6. Abort a Merge (if needed)

```bash
git merge --abort
```

---

# Git Commands to Restore Code (Before Commiting)
---

## 1. **Restore a file to last committed state**

```bash
git restore <file>
```
---

## 2. **Discard all local changes (not staged)**

```bash
git restore .
```

or:

```bash
git checkout -- .
```

---

## 3. **Unstage a file (but keep changes)**

```bash
git restore --staged <file>
```

---

## 4. **Restore file from a specific commit**

```bash
git restore --source=<commit_hash> <file>
```

---
# Git Commands to Revert Code (After Commiting)

## Syntax

```bash
git revert <commit_hash>
```

```bash
# To get all previous commit_hash:

git log --oneline
```


1. **Revert a single commit**

```bash
git revert a1b2c3d
```

→ Creates a new commit undoing commit `a1b2c3d`.

2. **Revert multiple commits**

```bash
git revert a1b2c3d..d4e5f6g
```

→ Reverts a range of commits (exclusive of first, inclusive of last).

3. **Revert last commit**

```bash
git revert HEAD
```

4. **Revert but don’t auto-commit (manual edit first)**

```bash
git revert --no-commit a1b2c3d
git commit -m "Reverted bad commit"
```
---

# Git Commands to Reset Code



## Syntax

```bash
git reset [--soft | --mixed | --hard] <commit_hash>
```

If no mode is given, Git uses `--mixed` by default.

---

## Modes of `git reset`

### 1. **Soft reset (`--soft`)**

* Moves HEAD to target commit.
* Keeps changes **staged** (in index).
* Useful if you want to **redo the last commit** but keep changes staged.

```bash
git reset --soft HEAD~1
```

Undo last commit, but files remain staged.

---

### 2. **Mixed reset (`--mixed`)** (default)

* Moves HEAD to target commit.
* Keeps changes in **working directory**, but unstages them.
* Useful to **rebuild staging area**.

```bash
git reset HEAD~1
```

Undo last commit, changes stay in working directory (unstaged).

---

### 3. **Hard reset (`--hard`)**

* Moves HEAD to target commit.
* Discards **everything** in staging and working directory.
* Dangerous — permanently deletes uncommitted work.

```bash
git reset --hard HEAD~1
```

Completely erases last commit and changes.

---

## Examples

1. **Undo last commit but keep changes staged**

```bash
git reset --soft HEAD~1
```

2. **Undo last commit and unstage changes**

```bash
git reset --mixed HEAD~1
```

3. **Completely erase last commit**

```bash
git reset --hard HEAD~1
```

4. **Reset branch to remote (discard local work)**

```bash
git fetch origin
git reset --hard origin/main
```

---

## When to Use

* **`--soft`** → If you committed too early, want to amend.
* **`--mixed`** → If you staged wrong files.
* **`--hard`** → If you want to throw away all local changes.

---
# Quick Comparison

| Command   | What it affects                             | Rewrites history? | Typical use                   |
| --------- | ------------------------------------------- | ----------------- | ----------------------------- |
| `restore` | Working directory / staging                 | ❌ No              | Discard local file changes    |
| `reset`   | HEAD (branch pointer), staging, working dir | ✅ Yes             | Undo commits (private work)   |
| `revert`  | Commit history (adds new commit)            | ❌ No              | Undo commits (shared history) |

---
