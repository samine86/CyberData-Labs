
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

## 8. Creating a New Branch
```bash
git checkout -b <new-branch-name>
```
Creates **and** switches to a new branch.  
Example: `git checkout -b feature/my-new-feature`

---

## 9. Switching Branches
```bash
git checkout <branch-name>
```
Switches to an existing branch.

---

## 10. Merging a Branch
```bash
git merge <branch-name>
```
Merges the specified branch into your current branch.

---

## 11. Checking Remote Configuration
```bash
git remote -v
```
Shows which remote repo(s) you have linked and their URLs.

---

## 12. Personal Access Token (For HTTPS Push)
When GitHub asks for a password during `git push`, use your **Personal Access Token** instead of your GitHub password.

---

### Additional Tips
- **Ctrl + C** cancels a running command if you get stuck.
- **ls**, **pwd**, **cd** are basic Bash commands often used alongside Git.
```
