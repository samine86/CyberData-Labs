# ✅ Git Basics — Clean and Structured Guide

## ➡️ 1. Configure Global Username & Email
```bash
git config --global user.name "YourName"
git config --global user.email "YourEmail@example.com"
```
- **Why:** Sets your identity for all commits on this machine.
- **When to use:** Only once when setting up Git.

---

## ➡️ 2. Cloning a Repository
```bash
git clone https://github.com/USERNAME/REPO-NAME.git
```
- **Why:** Creates a local copy of a remote repository.
- **When to use:** When starting to work with an existing repo.

---

## ➡️ 3. Checking Repository Status
```bash
git status
```
- **Why:** Shows which files are changed, staged, or untracked.
- **When to use:** Before staging, committing, pulling, or pushing.

---

## ➡️ 4. Staging Changes
```bash
git add <file-or-folder>
```
- Stages specific changes.
```bash
git add .
```
- Stages all modified/untracked files.

- **Why:** Prepares files for commit.
- **When to use:** Before committing.

---

## ➡️ 5. Committing Changes
```bash
git commit -m "Your commit message"
```
- **Why:** Saves a snapshot of changes.
- **When to use:** After staging changes.

---

## ➡️ 6. Pushing to Remote Repository
```bash
git push
```
- **Why:** Sends local commits to GitHub.
- **When to use:** After committing changes locally.

---

## ➡️ 7. Viewing Commit History
```bash
git log
```
- Shows detailed commit history.
```bash
git log --oneline -5
```
- Shows the last 5 commits in compact form.

- **Why:** To review commit history.
- **When to use:** Before pulling or when tracking changes.

---

## ➡️ 8. Checking Remote Configuration
```bash
git remote -v
```
- **Why:** Confirms the linked remote repository.
- **When to use:** After cloning or if in doubt about remote setup.

---

## ➡️ 9. Using Personal Access Token (For HTTPS Push)
- When GitHub asks for a password during `git push`, use a **Personal Access Token** instead of your GitHub password.
- **Why:** GitHub no longer supports password authentication.

---

## ➡️ 10. Pulling Updates from Remote Repository
```bash
git pull origin main
```
- Pulls updates if the main branch is `main`. 
- If the default branch is `master`:
```bash
git pull origin master
```
- **Why:** To sync local code with the latest changes from GitHub.
- **When to use:** Before pushing or starting new work.

---

## ➡️ 11. Handling Local Changes Before Pulling
### Option 1: Commit Changes
```bash
git add .
git commit -m "Save local changes before pulling updates"
git pull origin main
```
### Option 2: Use Git Stash
```bash
git stash
git pull origin main
git stash pop
```
- **Why:** Safely save changes without committing before pulling updates.
- **When to use:** If you’re not ready to commit but need to pull.

---

## ➡️ 12. Staging Deleted Files
```bash
git add -u
```
- **Why:** Stages modified and deleted files.
- **When to use:** After deleting files locally and before committing.

---

## ✅ Helpful Tips
- Press `Ctrl + C` to cancel any running Git command.
- Always use `git status` before pulling or pushing.
- Basic Bash navigation (`ls`, `pwd`, `cd`) helps you work alongside Git.

---

✨ **Update this file whenever new Git techniques are learned!**
