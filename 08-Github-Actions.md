# GitHub Actions

* It’s a **CI/CD (Continuous Integration / Continuous Deployment) tool** built into GitHub.
* Lets you **automate tasks** whenever something happens in your repo (like push, pull request, release).
* You define steps in a file called a **workflow** (YAML format).

---

### 🔹 What you can do with it

* Run tests automatically when you push code.
* Build and deploy apps (to GitHub Pages, AWS, Docker, etc.).
* Run linting, formatting, or security checks.
* Automate repetitive tasks (like labeling issues, sending notifications).

---

### 🔹 How it works

1. You create a `.github/workflows/` folder in your repo.
2. Inside, add a YAML file (e.g., `ci.yml`).
3. Define:

   * **Trigger** → When should it run? (on push, pull_request, schedule, etc.)
   * **Jobs** → What should it do? (build, test, deploy).
   * **Steps** → The actual commands or pre-made actions to run.

---

### 🔹 Example Workflow (simple CI)

```yaml
name: CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'
      - run: npm install
      - run: npm test
```

This workflow:

* Runs every time you **push code**.
* Checks out your repo.
* Installs Node.js and dependencies.
* Runs your tests.

---

In short:
**GitHub Actions = “Automation inside GitHub, triggered by events, running workflows to save you manual work.”**

---

# Github Workflows

## Key Concepts

### 1. **Workflow**

* A **YAML file** in `.github/workflows/`.
* Defines the automation.
* Example: “Run tests whenever I push code.”

---

### 2. **Event**

* The **trigger** that starts a workflow.
* Examples:

  * `push` → when code is pushed.
  * `pull_request` → when a PR is opened.
  * `schedule` → run every day at midnight.
  * `workflow_dispatch` → manual trigger.

---

### 3. **Job**

* A **set of steps** that run together on the same machine.
* Each workflow can have one or many jobs.
* Jobs can run **in parallel** or depend on each other.

Example jobs: `build`, `test`, `deploy`.

---

### 4. **Step**

* A **single task** inside a job.
* Runs either:

  * a shell command (`run: npm install`)
  * or a reusable action (`uses: actions/checkout@v3`).
* Steps inside a job run **sequentially**.

---

### 5. **Runner**

* The **machine** that runs the job.
* GitHub provides:

  * **Hosted runners** (like `ubuntu-latest`, `windows-latest`, `macos-latest`).
* You can also use a **self-hosted runner** (your own server/VM).

---

## Flow Summary

**Event → triggers Workflow → Workflow runs Jobs → Jobs run Steps → Steps run on a Runner.**

---

In short:

* **Workflow** = recipe file
* **Event** = what starts cooking
* **Job** = a dish to prepare
* **Step** = each instruction in the recipe
* **Runner** = the kitchen where it happens

---

