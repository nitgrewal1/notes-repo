# GitHub for a Complete Beginner — Summary Guide

## What Git and GitHub Are

- **Git** — a tool installed on your computer that tracks changes to your files over time.
- **GitHub** — a website that hosts your Git projects online so you can back them up, share them, or collaborate.

## Core Concepts

| Term | Meaning |
|---|---|
| Repository (repo) | A project folder with full change history |
| Commit | A saved snapshot of changes, with a message describing what changed |
| Branch | A separate line of work (default branch is usually `main`) |
| Push / Pull | Sending local changes to GitHub / pulling others' changes down |
| Pull Request (PR) | A request to merge one branch's changes into another |

---

## One-Time Setup

1. **Create a GitHub account** at [github.com](https://github.com)
2. **Install Git**
   - Windows: download from [git-scm.com](https://git-scm.com)
   - Mac: `git --version` in Terminal (prompts install if missing)
   - Linux: `sudo apt install git`
   - Verify: `git --version`
3. **Set your identity** (attached to every commit you make):
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your@email.com"
   ```

---

## Organizing Notes Before Uploading

A suggested folder structure for mixed `.md` + `.html` notes:

```
notes-repo/
├── README.md                 ← top-level index
├── cybersecurity/
│   ├── networking/
│   ├── web-exploitation/
│   ├── ctf-writeups/
│   └── tools/                ← interactive HTML notes/explainers
├── finance/
│   ├── concepts/
│   └── tools/                ← HTML dashboards/calculators
├── mythology/
└── assets/                   ← shared images/diagrams
```

**Conventions:**
- Lowercase, hyphen-separated filenames: `sql-injection-basics.md`
- Number prefixes for sequential notes: `01-nmap-basics.md`
- A `README.md` in every folder acting as a mini table of contents
- Enable **GitHub Pages** (Settings → Pages → Deploy from branch → `main` → root) to view `.html` files as rendered pages instead of raw code

---

## Step 1: Place Your Files

Unzip your prepared folder, drop your real `.md`/`.html` files into the matching subfolders, then open a terminal **inside that folder**:

```bash
cd /path/to/notes-repo
pwd        # confirms your current location (Mac/Linux)
```

---

## Step 2: Turn the Folder into a Git Repository (once per project)

```bash
git init                          # start tracking this folder with Git
git add .                         # stage all files (like adding to a cart)
git commit -m "Initial structure" # save the first permanent snapshot
```

- `git init` — only run once per project, ever.
- `git add` and `git commit` are repeated every time you want to save new changes.

---

## Step 3: Push to GitHub (once per project)

**A. Create an empty repo on GitHub**
1. github.com → **+** → **New repository**
2. Name it (e.g. `notes-repo`)
3. Leave it completely empty — do **not** check "Add a README"
4. Click **Create repository** and copy the URL shown (e.g. `https://github.com/your-username/notes-repo.git`)

**B. Connect and push**
```bash
git remote add origin https://github.com/your-username/notes-repo.git
git branch -M main
git push -u origin main
```

**C. Authentication**
GitHub no longer accepts your account password for this. Either:
- Approve via the browser popup if one appears, or
- Use a **Personal Access Token** as the "password": GitHub → profile photo → **Settings** → **Developer settings** → **Personal access tokens** → **Tokens (classic)** → **Generate new token** → check `repo` scope → generate → copy it immediately (shown only once)

After pushing, refresh your repo page on GitHub — your files should all be visible there.

---

## Ongoing Workflow (every time you update notes)

```bash
git add .
git commit -m "short description of what changed"
git push
```

---

## Important Detail: Commit Messages

`git commit` always requires a message.

```bash
git commit          # opens a text editor (often Vim) — must type a message there
git commit -m "msg" # skips the editor, message given inline — easier for beginners
```

If Vim opens unexpectedly: press `i` to type, `Esc` when done, then `:wq` + Enter to save and quit.

There's a force-empty option (`git commit --allow-empty-message -m ""`), but it's not recommended — empty messages make your history hard to understand later.
