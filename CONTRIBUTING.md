# How to contribute

You are adding **one new file** to `entries/`. Pick a short unique name, for example `fetch-vs-pull-7421.md`: lowercase letters, digits and hyphens, 3 to 41 characters, ending in `.md`. A random number helps avoid name clashes.

Use this content (copy from [`entries/_TEMPLATE.md`](entries/_TEMPLATE.md)):

```
# What I learned

# A useful tip

# What I wish the session covered
```

Write your text under each heading. English or Arabic is fine.

## Path A: in your browser (no Git needed)

1. Sign in to GitHub. Two-factor authentication is required for contributors.
2. Open the `entries` folder, then **Add file → Create new file**. GitHub will offer to fork the repository for you.
3. In the name box type `entries/your-short-name.md`.
4. Paste the template and fill it in.
5. Click **Commit changes…**, choose **Propose changes**, then **Create pull request**.
6. Fill in the checklist, and wait for the automatic check. A maintainer may need to approve it to run. That is normal for first-time contributors.

## Path B: with Git commands

```
git clone https://github.com/<you>/trust-issues-feedback.git   # your fork
cd trust-issues-feedback
git switch -c entry/your-short-name
cp entries/_TEMPLATE.md entries/your-short-name.md             # then edit it
git status
git add entries/your-short-name.md                              # not "git add ."
git diff --staged                                               # read what you are about to commit
git commit -m "Add entry: your-short-name"
git fetch origin
git log --oneline origin/main..HEAD                             # what you are about to push
git push -u origin entry/your-short-name
```

Then open a Pull Request on GitHub. If `origin` is your fork, add the original repository as `upstream` to stay up to date.

## If the check fails

Open the failed check and read the message. Fix your file, commit, and push again: the Pull Request updates itself.
