# 1. Global Git Aliases

Global aliases apply to **all repositories** for your user.

### Steps

1. Open terminal (anywhere).
2. Run:

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm "commit -m"
git config --global alias.st status
git config --global alias.last "log -1 HEAD"
```

### Example usage

```bash
git co main         # instead of git checkout main
git br              # instead of git branch
git cm "Fix bug"    # instead of git commit -m "Fix bug"
git st              # instead of git status
git last            # show last commit
```

---

# 2. Local Git Aliases

Local aliases apply to **only one repository**.

### Steps

1. Navigate into your repo:

```bash
cd my-project
```

2. Run:

```bash
git config alias.co checkout
git config alias.br branch
```

Now inside `my-project` repo, only these shortcuts will work.

---

# 3. Verify Aliases

To list aliases:

```bash
git config --global --get-regexp alias
```

(for global ones)

or

```bash
git config --get-regexp alias
```

(for local ones).

---

✅ **Global** → applies everywhere. \
✅ **Local** → only for that repo.

---
