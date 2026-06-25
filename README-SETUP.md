# Setup Guide

Follow these steps to get your Fly Fishing Library live on GitHub Pages.

---

## Step 1: Create the GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click **New repository**
3. Name it `fly-fishing-library`
4. Set it to **Private** (recommended) or Public
5. **Do not** initialize with a README (you'll push this folder)
6. Click **Create repository**

---

## Step 2: Push This Folder to GitHub

In your terminal, from inside this folder:

```bash
git init
git add .
git commit -m "Initial commit: fly fishing library scaffold"
git branch -M main
git remote add origin https://github.com/YOURUSERNAME/fly-fishing-library.git
git push -u origin main
```

Replace `YOURUSERNAME` with your actual GitHub username.

---

## Step 3: Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **GitHub Actions**
4. Save

The first deploy will trigger automatically after your push. It takes about 60 seconds. Your site will be live at:

```
https://YOURUSERNAME.github.io/fly-fishing-library
```

---

## Step 4: Update _config.yml

Open `_config.yml` and update these two lines:

```yaml
url: "https://YOURUSERNAME.github.io"
```

Commit and push that change.

---

## Step 5: Connect GitHub MCP to Your Claude Project

1. In Claude.ai, open your fly fishing Claude Project
2. Go to **Project settings** → **Integrations** (or the connectors/tools menu)
3. Search for **GitHub** and connect it
4. Authorize Claude to access your `fly-fishing-library` repository

Once connected, paste the contents of `CLAUDE-PROJECT-INSTRUCTIONS.md` into your Claude Project's **System Prompt** field.

---

## Step 6: Test It

Ask your Claude project:

> "Create a new species doc for Bluegill and commit it to the repo."

Within about a minute, the site should rebuild and the new page will appear live.

---

## Ongoing Workflow

- **Add new docs:** Ask Claude to create them; it commits directly
- **Update existing docs:** Ask Claude to read and update; it re-commits
- **Every commit auto-deploys** via GitHub Actions — no manual steps needed
- **View history:** Go to your repo → **Commits** to see every change Claude made

---

## Local Preview (Optional)

If you want to preview changes locally before pushing:

```bash
# Install Ruby and Bundler first, then:
bundle install
bundle exec jekyll serve
# Open http://localhost:4000/fly-fishing-library
```
