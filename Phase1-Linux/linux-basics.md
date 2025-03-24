# 🐧 Linux Basics — Detailed Explanations

## ✅ 1. Navigation Commands

### ➡️ `pwd`
- **What it does:** Prints the current directory you are in (Print Working Directory).
- **Why use it:** Helps you confirm where you are in the file system.

### ➡️ `ls`
- **What it does:** Lists all files and folders in the current directory.
- **Why use it:** Quickly see available files and directories.

### ➡️ `ls -l`
- **What it does:** Lists files with detailed info (permissions, size, owner, last modified).
- **Why use it:** To check file ownership and permissions.

### ➡️ `cd foldername`
- **What it does:** Changes directory to `foldername`.
- **Why use it:** To move around the file system.

### ➡️ `mkdir foldername`
- **What it does:** Creates a new directory.
- **Why use it:** Organize files into folders.

### ➡️ `rmdir foldername`
- **What it does:** Removes an empty directory.
- **Why use it:** Clean up unused folders.

## ✅ 2. File Operations

### ➡️ `touch filename`
- **What it does:** Creates an empty file with the given name.
- **Why use it:** Quickly create placeholder files for practice or testing.

### ➡️ `rm filename`
- **What it does:** Removes (deletes) the file.
- **Why use it:** Clean up unwanted files.

### ➡️ `cat filename`
- **What it does:** Displays the content of the file.
- **Why use it:** Quickly read small text files.

### ➡️ `nano filename`
- **What it does:** Opens the file in a simple text editor in the terminal.
- **Navigation in nano:**
  - **Ctrl + O**: Save file
  - **Ctrl + X**: Exit nano
  - **Ctrl + K**: Cut a line
  - **Ctrl + U**: Paste the line

## ✅ 3. Permissions and Ownership

### ➡️ `ls -l filename`
- **What it does:** Displays permissions (r=read, w=write, x=execute) for owner, group, others.
- Example: `-rw-r--r--` means owner can read/write; group and others can only read.

### ➡️ `chmod 755 filename`
- **What it does:** Changes file permissions.
- `7` (rwx), `5` (r-x) — This command gives full permission to the owner, and read/execute to others.
- **Why use it:** Control who can read, write, or execute a file.

### ➡️ `chown username:groupname filename`
- **What it does:** Changes the file owner and group.
- **Why use it:** Manage file ownership for security and proper access.

## ✅ 4. Process Management

### ➡️ `ps aux`
- **What it does:** Shows all running processes with user, CPU usage, memory usage, PID.
- **Why use it:** Check what’s running and how resources are used.

### ➡️ `ps aux | less`
- **What it does:** Shows all processes but allows scrolling through output.
- **Why use it:** When output is too long, `less` lets you scroll up/down.
- **How to navigate:**
  - Use Up/Down keys or PageUp/PageDown.
  - Press `q` to exit back to terminal.

### ➡️ `top`
- **What it does:** Displays real-time updates of system resource usage.
- **Why use it:** Monitor what’s consuming CPU and memory.

### ➡️ `htop` (if installed)
- **What it does:** An interactive and colorful real-time process viewer.
- **Why use it:** Easier to navigate than `top`.

### ➡️ `kill PID`
- **What it does:** Terminates a process with the given Process ID.
- **Why use it:** Stop unresponsive or unwanted processes.

## ✅ 5. Network Basics (Intro Preview)

### ➡️ `ip a`
- **What it does:** Shows all network interfaces and their IP addresses.
- **Why use it:** Check local IP address and network interface statuses.

### ➡️ `ip route | grep default`
- **What it does:** Displays the default gateway (router IP).
- **Why use it:** Know your network’s gateway for troubleshooting.

---

✨ **As you learn more commands, add them to this file with detailed explanations.**
