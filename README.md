# Soccer Trivia — Privacy Policy site

A single static `index.html` that hosts the bilingual (Hebrew + English) privacy policy
for **Israeli Soccer Trivia / טריוויה כדורגל ישראלי**.

This is the file that gets served at the **Privacy Policy URL** submitted to Google Play
(`App content → Privacy policy`). Google Play requires the URL to be:

- active and reachable
- non-editable, non-commentable
- not a PDF
- not password-protected
- publicly accessible from anywhere
- not auto-downloading a file

A **Gist** was rejected on 2026-05-06 because Gists are commentable by logged-in GitHub
users and forkable. A static HTML page on GitHub Pages avoids both issues.

## Deploy in 5 minutes (GitHub Pages)

1. On github.com, create a new **public** repo, e.g. `soccer-trivia-privacy`.
   Don't initialize it with anything.
2. From this directory:
   ```bash
   cd store/privacy_site
   git init -b main
   git add index.html README.md
   git commit -m "Add privacy policy page"
   git remote add origin https://github.com/<your-gh-user>/soccer-trivia-privacy.git
   git push -u origin main
   ```
3. On the new repo: **Settings → Pages**.
   - **Source:** Deploy from a branch
   - **Branch:** `main` / `(root)`
   - Save.
4. Within ~1 minute the URL will be live at:
   `https://<your-gh-user>.github.io/soccer-trivia-privacy/`
5. Open it in an incognito tab from your phone — confirm it renders, no auto-download,
   no login required.
6. Play Console → **App content → Privacy policy** → paste that URL → Save.
7. Resubmit the rejected release for review.

## Why a separate repo and not the main code repo?

`store/UPLOAD_GUIDE_HE.md` contains the upload keystore password and SHA fingerprints.
Don't push the main project repo public. A dedicated single-page repo keeps the
privacy site fully isolated.

## Updating the policy later

Edit `index.html`, bump the **Effective date** in both language sections, commit, push.
GitHub Pages re-deploys automatically; the URL stays the same so Play doesn't need to
re-review the URL itself (only the policy content if it materially changes).
