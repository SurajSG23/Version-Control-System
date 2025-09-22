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

# Git Commands to Restore Code
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

