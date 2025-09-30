
# Git Stach Command

`git stash` is used to **temporarily save your uncommitted changes** (both staged and unstaged) **without committing them**.
It gives you a clean working directory so you can switch branches or pull updates safely.

---

### 🔹 How it works

1. You run:

   ```bash
   git stash
   ```

   → Your changes are saved in a "stash stack" and removed from your working directory.

2. Later, you can bring them back with:

   ```bash
   git stash apply
   ```

   (or `git stash pop` which applies *and removes* it from the stash stack).

---

### 🔹 Useful Commands

* Save changes:

  ```bash
  git stash
  ```
* Show list of stashes:

  ```bash
  git stash list
  ```
* Apply latest stash:

  ```bash
  git stash apply
  ```
* Apply and remove from stash:

  ```bash
  git stash pop
  ```
* Drop a specific stash:

  ```bash
  git stash drop stash@{0}
  ```

---

### 🔹 When to use it

* You’re in the middle of work, but need to:

  * Switch to another branch quickly.
  * Pull new changes from remote.
  * Work on a hotfix without committing half-done code.

---

In short:
**`git stash` = “Put my unfinished work in a temporary drawer, I’ll pick it up later.”**

---
