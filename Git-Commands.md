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
## 3. Add Remote Repository

```bash
git remote add origin https://github.com/username/repository.git
```

## 4. Commit Changes

```bash
git commit -m "Initial commit"
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
