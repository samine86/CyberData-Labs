# 🐧 Linux Basics — Detailed Explanations

## ✅ 1. Navigation Commands

### ➡️ `pwd` (Print Working Directory)
- **What it does:** Shows the full path of the current directory.
- **Why use it:** Helps confirm where you are in the file system.

### ➡️ `ls` (List Files)
- **What it does:** Lists files and directories in the current location.
- **Variations:**
  - `ls -l` — Detailed listing (permissions, size, owner).
  - `ls -a` — Shows hidden files (files starting with `.`).
  - `ls -la` — Combined view (detailed + hidden files).

### ➡️ `cd` (Change Directory)
- **What it does:** Moves between directories.
- **Usage Examples:**
  - `cd foldername` — Move into a folder.
  - `cd ..` — Move up one directory.
  - `cd ~` — Move to home directory.
  - `cd /` — Move to the root directory (`/`).
- **Note:** In Git Bash, `C:\` is accessed as `/c/`.

### ➡️ `mkdir foldername`
- **What it does:** Creates a new folder.
- **Usage Example:**
```bash
mkdir testfolder
```

---

## ✅ 2. File Operations

### ➡️ `touch filename`
- **What it does:** Creates an empty file with the given name.
- **Usage Example:**
```bash
touch myfile.txt
```

### ➡️ `rm filename`
- **What it does:** Deletes a file.
- **Usage Example:**
```bash
rm myfile.txt
```

### ➡️ `cat filename`
- **What it does:** Displays the contents of a file.
- **Usage Example:**
```bash
cat myfile.txt
```

### ➡️ `nano filename`
- **What it does:** Opens a simple text editor in the terminal.
- **Nano Shortcuts:**
  - `Ctrl + O` — Save changes
  - `Ctrl + X` — Exit
  - `Ctrl + K` — Cut line
  - `Ctrl + U` — Paste line

---

## ✅ 3. File Permissions & Ownership

### ➡️ `ls -l` (Check File Permissions)
- **What it does:** Shows file permissions in detail.
- **Example Output:**
```bash
-rw-r--r-- 1 pi pi 4096 Apr 20 10:00 myfile.txt
drwxr-xr-x 2 pi pi 4096 Apr 20 10:05 myfolder
```
- First character: `-` (file) or `d` (directory).
- Permissions in three groups: `rwxr-xr-x` (owner, group, others).
- `r` = read, `w` = write, `x` = execute.

### ➡️ `chmod` (Change File Permissions)
- Add execute permission for user:
```bash
chmod u+x test.sh
```
- Remove write permission for group:
```bash
chmod g-w test.sh
```
- Numeric permission example:
```bash
chmod 755 myscript.sh
```
- `7` (rwx), `5` (r-x) — Full permissions for owner, read-execute for others.

### ➡️ `chown` (Change File Ownership)
- Change owner and group:
```bash
sudo chown newuser:newgroup myfile.txt
```
- Example:
```bash
sudo chown alex:alex test.sh
```

---

## ✅ 4. Process Management

### ➡️ `ps aux` (List Running Processes)
- **What it does:** Shows active processes with CPU, memory usage, and users.
- **Key Information:** PID (process ID), CPU%, memory%, command.

### ➡️ `ps aux | less` (Scrollable Process List)
- **What it does:** Displays processes with scrollable output.
- **Navigation:**  
  - Arrow keys / PageUp / PageDown to scroll  
  - `q` to quit

### ➡️ `top` (Real-time System Monitor)
- **What it does:** Shows live CPU and memory usage.
- **Navigation Tips:**  
  - `Shift + M` — Sort by memory  
  - `Shift + P` — Sort by CPU  
  - `q` — Quit

### ➡️ `htop` (Improved Interactive Monitor)
- Install:
```bash
sudo apt-get install htop
```
- Run:
```bash
htop
```
- `F10` or `q` — Quit

### ➡️ `kill` (Terminate Process)
- Kill a process:
```bash
kill <PID>
```
- Force kill if needed:
```bash
kill -9 <PID>
```
> ⚠️ Use `kill -9` carefully — it forcefully stops the process.

---

## ✅ 5. Finding Files & Text

### ➡️ `find` (Search for Files by Name)
- Example:
```bash
find /home/pi -name "myfile.txt"
```

### ➡️ `grep` (Search for Text in Files)
- Example:
```bash
grep "error" /var/log/syslog
```

---

## ✅ Command Recap Table

| **Command**                      | **Description**                               |
|----------------------------------|-----------------------------------------------|
| `pwd`                            | Shows current directory                       |
| `ls -l`                          | Lists files with details                      |
| `cd foldername`                  | Change directory                              |
| `mkdir foldername`               | Create new directory                          |
| `rm filename`                    | Delete a file                                 |
| `nano filename`                  | Open file in nano editor                      |
| `chmod 755 filename`             | Change file permissions                       |
| `chown user:group filename`      | Change file ownership                         |
| `ps aux`                         | Show running processes                        |
| `kill PID`                       | Terminate a process by PID                    |
| `top`                            | Real-time CPU and memory monitoring           |
| `find /home -name \"file.txt\"`  | Find a file by name                           |
| `grep \"word\" file.txt`         | Search for a word inside a file               |

---

✨ **As you learn more commands, add them to this file with full explanations!**
