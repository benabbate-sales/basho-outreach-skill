# Pushing with GitHub Desktop (no terminal needed)

You've already created the empty repo at `github.com/benabbate-sales/basho-outreach-skill`. These steps use GitHub Desktop (already installed on your Mac) instead of the terminal to push the files.

## 1. Move the folder somewhere permanent

The `basho-outreach-skill` folder is currently in Cowork's outputs. Drag it out to somewhere on your Mac — e.g. `~/Documents/basho-outreach-skill` or `~/Developer/basho-outreach-skill`. Anywhere you'll remember.

## 2. Open GitHub Desktop → Add Local Repository

1. In GitHub Desktop: top-left menu → **File → Add Local Repository…**
2. Click **Choose…** and pick the `basho-outreach-skill` folder you just moved.
3. You'll see a warning: *"This directory does not appear to be a Git repository. Create a repository?"* Click the blue **create a repository** link in that warning.

## 3. Fill in the "Create a New Repository" dialog

- **Name:** `basho-outreach-skill` (should auto-fill)
- **Description:** *A Claude skill for drafting basho-style first-touch emails.*
- **Local Path:** leave as-is
- **Initialize this repository with a README:** ❌ leave unchecked (we already have one)
- **Git Ignore / License:** leave as **None** for both (we already have those too)

Click **Create Repository**.

## 4. Publish to GitHub

Top of the window you'll now see a blue button **Publish repository**. Click it.

A dialog appears:

- **Name:** `basho-outreach-skill`
- **Description:** already filled
- **Keep this code private:** ❌ **uncheck this** (the repo on GitHub is public; this must match)
- **Organization:** leave as your account (`benabbate-sales`)

Click **Publish Repository**.

GitHub Desktop will push the files to your already-created GitHub repo. Takes a few seconds.

## 5. Check it worked

Open the GitHub repo page in Chrome:

`https://github.com/benabbate-sales/basho-outreach-skill`

You should see:

- README rendered on the home page
- `skills/` folder visible
- `CONFIG.md`, `LICENSE`, `.gitignore` listed

If yes — you're done. Share the URL.

---

## Troubleshooting

**"Publish repository" tries to create a new repo, but one with that name already exists.**
Your empty repo on GitHub and the local one aren't matched up yet. Easiest fix: go to `https://github.com/benabbate-sales/basho-outreach-skill` on the web, click **Settings → Delete this repository**, confirm. Then retry step 4 — GitHub Desktop will create it fresh.

**GitHub Desktop asks you to sign in.**
Use the "Sign in to GitHub.com" button. It'll open a browser auth flow. After signing in, come back to GitHub Desktop and retry.

**Files aren't showing on github.com after pushing.**
Hit refresh on the GitHub page. If still empty, in GitHub Desktop check the left sidebar for **History** — the commit should be there. If it is but didn't push, click **Push origin** at the top.
