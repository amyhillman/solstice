---
name: publish-solstice-site
description: >-
  Publishes the static Project Solstice site by committing and pushing
  index.html to main so GitHub Pages (amyhillman.github.io/solstice) updates.
  Use when the user replaced or edited solstice/index.html, saved, and asks to
  publish, deploy, go live, commit and push, or sync GitHub Pages.
disable-model-invocation: false
---

# Publish Solstice site (GitHub Pages)

## Preconditions

- Workspace is the **solstice** repo (site file is **`index.html`** at repo root).
- User has **saved** their changes (**⌘S**). If `git status` shows no changes to `index.html`, tell them to save or confirm they edited the file under this repo path.

## Steps

1. `cd` to repo root; run `git status` and `git diff --stat index.html` (or full diff if small).
2. If there is **nothing to commit**: stop and explain (unsaved buffer, wrong folder, or identical file).
3. If there are changes: **`git add index.html`**, then **`git commit`** with a short message that reflects the *substance* of the edit (review diff for wording).
4. **`git push origin main`** (no `--force` on `main`).
5. Tell the user: GitHub Pages often updates in **1–3 minutes**, sometimes up to **~10**; suggest a **hard refresh** (⌘⇧R) if the old page persists.

## Do not

- Commit unrelated files unless the user explicitly asked to include them.
- Force-push `main` or skip hooks unless the user explicitly requested that.
