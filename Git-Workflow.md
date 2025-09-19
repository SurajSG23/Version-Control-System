# Local Repo, Remote Repo, and Git Workflow

## Local Repository
- Exists on your computer.
- Created using:
```bash
git init
````

* All commits, branches, and history are stored locally.
* You can work offline.

## Remote Repository

* Hosted on a server (e.g., GitHub, GitLab, Bitbucket).
* Shared with team members for collaboration.
* Connected to local repo using:

```bash
git remote add origin https://github.com/username/repository.git
```

---

## Git Workflow (Basic)

### 1. Clone Remote Repo (first time only)

```bash
git clone https://github.com/username/repository.git
```

### 2. Create/Work on a Branch

```bash
git checkout -b feature-branch
```

### 3. Make Changes Locally

* Edit files
* Check status:

```bash
git status
```

### 4. Stage and Commit

```bash
git add .
git commit -m "Describe changes"
```

### 5. Pull Latest Changes (sync with remote)

```bash
git pull origin main
```

### 6. Push Branch/Changes

```bash
git push origin feature-branch
```

### 7. Open Pull Request (on GitHub)

* Review and merge into `main`.

---

## Summary

* **Local repo** → your copy on your machine.
* **Remote repo** → shared repo on GitHub (or similar).
* **Workflow** → clone → branch → edit → add → commit → pull → push → PR/merge.

---
