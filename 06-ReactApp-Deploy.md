## Step 1: Install `gh-pages`

In your project folder, run:

```bash
npm install gh-pages --save-dev
```

---

## Step 2: Update `vite.config.js`

Add the `base` property so GitHub knows where to serve your app.

Example (if your repo name is `my-app`):

```js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [react()],
  base: '/my-app/', // your repo name here
})
```

---

## Step 3: Update `package.json`

Add `homepage` and deployment scripts.

```json
{
  "name": "my-app",
  "version": "0.0.1",
  "private": true,
  "homepage": "https://<your-username>.github.io/my-app", // your repo url here
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist"
  }
}
```

* Replace `<your-username>` with your GitHub username.
* Replace `my-app` with your repo name.

---

## Step 4: Push Code to GitHub

Initialize repo if not done already:

```bash
git init
git remote add origin https://github.com/<your-username>/my-app.git
git add .
git commit -m "first commit"
git push -u origin main
```

---

## Step 5: Deploy

Run:

```bash
npm run deploy
```

This will:

* Build the app → output goes to `dist/`.
* Push `dist/` to a new branch called `gh-pages`.

---

## Step 6: Enable GitHub Pages

1. Go to your repo on GitHub.
2. Settings → Pages.
3. Set branch to **`gh-pages`**.
4. Save.

Your site will be live at:

```
https://<your-username>.github.io/my-app
```

---
