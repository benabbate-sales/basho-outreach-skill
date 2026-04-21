# Pushing this to GitHub

These are the exact steps to get the repo live under `github.com/benabbate-sales/basho-outreach-skill`. Don't paste this file into the repo — it's just for you.

## 1. Create the empty repo on github.com

1. Go to [github.com/new](https://github.com/new)
2. **Repository name:** `basho-outreach-skill`
3. **Owner:** `benabbate-sales`
4. **Public**
5. **Do NOT** check "Add a README file", "Add .gitignore", or "Add a license" — we already have those locally.
6. Click **Create repository**.

You'll land on a page with "…or push an existing repository from the command line" — ignore the commands shown there, use the ones below.

## 2. Install git (if you haven't already)

Check first:

```bash
git --version
```

If you get a version number, skip to step 3. If not, install from [git-scm.com](https://git-scm.com/downloads).

## 3. Push the files

Open Terminal and run these, one block at a time. **Replace the path in the first line** with wherever you downloaded the folder from Cowork.

```bash
cd ~/Downloads/basho-outreach-skill   # <-- change this to your actual path
git init
git add .
git commit -m "Initial commit: basho-outreach skill"
git branch -M main
git remote add origin https://github.com/benabbate-sales/basho-outreach-skill.git
git push -u origin main
```

The first time you push, GitHub may prompt you to authenticate. Easiest: install [GitHub CLI](https://cli.github.com/), then run `gh auth login` once before the `git push`.

## 4. Sanity check

Go to `https://github.com/benabbate-sales/basho-outreach-skill` — you should see the README rendered on the home page. If the skills table links are blue and clickable, you're done.

## Optional: add topics and a description on GitHub

On the repo page, click the ⚙️ next to "About" and add:

- **Description:** "A Claude skill for AEs — drafts basho-style first-touch emails with a research gate."
- **Topics:** `claude`, `claude-skills`, `sales`, `cold-email`, `basho`, `anthropic`

This makes the repo findable by anyone searching for Claude skills.
