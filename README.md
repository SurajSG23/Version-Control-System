# Version Control System (VCS) – Git & GitHub Notes

## What is Version Control System (VCS)?
A **Version Control System** is a tool that helps track changes to files (especially code) over time.  
It allows multiple developers to work together without overwriting each other’s work.  

### Benefits:
- Tracks history of changes
- Supports collaboration
- Allows rollback to previous versions
- Manages branches for parallel development
- Prevents code conflicts

---

## Git
**Git** is a distributed version control system created by Linus Torvalds (2005).  
It allows developers to keep a local copy of the project and sync with a remote repository.

### Key Features:
- Distributed (every developer has a full copy of repo)
- Lightweight branching & merging
- Tracks changes efficiently
- Works offline

### Common Git Commands
| Command | Description |
|---------|-------------|
| `git init` | Initialize a new Git repository |
| `git clone <url>` | Clone a remote repository |
| `git status` | Check current repo status |
| `git add <file>` | Stage changes for commit |
| `git commit -m "msg"` | Save changes to repo |
| `git log` | View commit history |
| `git branch` | List branches |
| `git checkout -b <branch>` | Create & switch to a new branch |
| `git merge <branch>` | Merge branch into current branch |
| `git push` | Upload commits to remote |
| `git pull` | Fetch + merge from remote |
| `git remote -v` | Show remote URLs |

---

## GitHub
**GitHub** is a cloud-based hosting service for Git repositories.  
It provides collaboration features and project management tools.

### Key Features:
- Host Git repositories online
- Collaborate with teams
- Pull requests (PRs) & code reviews
- Issues & project boards
- Actions (CI/CD automation)

---

## Git vs GitHub
| Feature | Git | GitHub |
|---------|-----|--------|
| Type | Tool (VCS) | Hosting platform |
| Use | Local version control | Remote collaboration |
| Offline support | ✅ Yes | ❌ No (requires internet) |
| Ownership | Open-source | Owned by Microsoft |

---

## Workflow Example
1. Create repo on GitHub  
2. Clone it locally → `git clone <url>`  
3. Make changes  
4. Stage files → `git add .`  
5. Commit → `git commit -m "Added feature"`  
6. Push → `git push origin main`  
7. Create Pull Request on GitHub (if working in team)  

---

## Summary
- **VCS** = Tracks changes  
- **Git** = Tool (local VCS)  
- **GitHub** = Online hosting + collaboration  

---
*With Git + GitHub, developers can build, track, and collaborate efficiently on any project.*
