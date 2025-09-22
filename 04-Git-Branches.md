### 🔹 Create a branch

```bash
git branch <branch_name>
```
### 🔹 Rename a branch

```bash
git branch -M <new_branch_name>
```

### 🔹 Switch to a branch

```bash
git checkout <branch_name>
# or (newer way)
git switch <branch_name>
```

### 🔹 Create + switch in one step

```bash
git checkout -b <branch_name>
# or
git switch -c <branch_name>
```

### 🔹 Merge a branch into current branch

```bash
git merge <branch_name>
```

### 🔹 Delete a branch (local)

```bash
git branch -d <branch_name>   # safe delete (if merged)
git branch -D <branch_name>   # force delete
```

### 🔹 Delete a branch (remote)

```bash
git push origin --delete <branch_name>
```

---
### 🔹 Display all branches

```bash
git branch
```

---
