# 🔹 `git fetch`

* Imagine GitHub has some **new commits**.
* `git fetch` will **download them** into your local Git system, but it won’t touch your current working branch.
* Your code files will **stay the same**.
* You can first **review** what changed (using `git log origin/main` or `git diff origin/main`).
* Merge the changes using `git merge origin\main`

Think of it like: *“Bring the news, but don’t update my notebook yet.”*

---

# 🔹 `git pull`

* `git pull` does **two steps at once**:

  1. Fetch → download changes.
  2. Merge (or rebase) → apply them to your current branch.
* Your code will be **updated immediately**.

Think of it like: *“Bring the news and write it into my notebook right now.”*

---

### Main Difference

* **Fetch** = safe, no immediate changes → good for checking first.
* **Pull** = quick, updates your code → good if you just want the latest version.

---