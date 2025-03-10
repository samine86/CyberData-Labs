
# Git Basics

## 1. Configure Global Username & Email
git config --global user.name "YourName"
git config --global user.email "YourEmail@example.com"
```
Sets your name and email for all Git commits on this machine.

---

## 2. Cloning a Repository
```bash
git clone https://github.com/USERNAME/REPO-NAME.git
```
Creates a local copy of the remote repository on your machine.
---

## 3. Checking Repository Status
```bash
git status
```
Shows changed files, untracked files, and which branch you’re on.

---

## 4. Staging Changes
```bash
git add <file-or-folder>
```
Moves changes into the “staging area” so they’re ready to be committed.

```bash
git add .
```
Stages all modified/untracked files in the current directory.

---

## 5. Committing Changes
```bash
git commit -m "Your commit message"
```
Records a snapshot of the staged changes with a message describing what changed.

---

## 6. Pushing to Remote Repository
```bash
git push
```
Sends your local commits to the remote repository (e.g., on GitHub).

---

## 7. Viewing Commit History
```bash
git log
```
Displays a chronological list of commits in your current branch.

---


## 8. Checking Remote Configuration
```bash
git remote -v
```
Shows which remote repo(s) you have linked and their URLs.

---

## 9. Personal Access Token (For HTTPS Push)
When GitHub asks for a password during `git push`, use your **Personal Access Token** instead of your GitHub password.

---

### Additional Tips
- **Ctrl + C** cancels a running command if you get stuck.
- **ls**, **pwd**, **cd** are basic Bash commands often used alongside Git.

---

## 10. Pulling Updates from GitHub (Sync Local Repo)
```bash
git pull origin main
```
- Downloads the latest changes from the remote repository (GitHub) into your local machine.
- If your default branch is `master`, use:
  ```bash
  git pull origin master
  ```

---

## 11. Checking Commit History
```bash
git log --oneline -5
```
- Shows the last **5 commits** in a compact format.

---

## 12. What to Do if You Have Local Changes

### Option 1: **Commit Your Local Changes Before Pulling**
```bash
git add .
git commit -m "Save local changes before pulling updates"
git pull origin main
```
- Saves your changes first before pulling new updates.

### Option 2: **Temporarily Save Changes with Stash**
```bash
git stash
git pull origin main
git stash pop
```
- `git stash` temporarily saves your changes.
- `git pull` gets the latest updates from GitHub.
- `git stash pop` restores your saved changes after the pull.

---

## 13. Checking Repository Status
```bash
git status
```
- Always check your repo's status before pulling or pushing.
```

---

## 14. Staging Deleted Files
```bash
git add -u
```
- Stages only **modified and deleted** files for commit.
- Useful when removing unwanted files from Git.
```
---

