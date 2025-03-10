# Linux Basics

## pwd
- Prints the current working directory.

## ls
- Lists files in the current directory.
- Lists files/folders, shows permissions, owners, etc.- Example: `ls -la` shows detailed info (permissions, owner, etc.).

## cd
- Changes the current directory.
- Note: In Git Bash, C:\ is /c/
- cd .. move to previous dir
- cd~

## mkdir
- Creates a new directory.
- Usage: `mkdir testfolder`.

## View & Edit a File:

- Nano editor
- example: nano myfile.txt

## Check the contents
- cat myfile.txt

## Remove a File
- rm myfile.txt

#  Task 2.1: File Permissions & Ownership

- chmod examples
- chown usage

## Check Permissions with ls -l

- ls -l
You’ll see something like:

-rw-r--r-- 1 pi pi  4096 Apr 20 10:00 myfile.txt
drwxr-xr-x 2 pi pi  4096 Apr 20 10:05 myfolder

The first character - or d indicates file (-) or directory (d).
Next 9 characters are permissions in 3 groups: rwxr-xr-x
r = read, w = write, x = execute, and - means that permission is absent.
The first set is for the owner, second set for the group, third set for others.

## Changing Permissions with chmod

Suppose you have a file test.sh. You want to make it executable for the owner only. You do:
- chmod u+x test.sh
u = user (owner), +x = add execute permission.

If you want to remove write permission for group:
- chmod g-w test.sh
g = group, -w = remove write.

## Changing Ownership with chown
To change the owner (user) and group of test.sh:
- sudo chown newowner:newgroup test.sh
For example, if you create a new user alex, you could do:
sudo chown alex:alex test.sh


### Task 2.2: Process Management
- ps aux usage
- top/htop usage
- killing processes

## ps Command

- ps
Lists processes in the current terminal session.

- ps aux
Shows all processes for all users in a detailed format.

## top or htop

top gives a real-time view of running processes (CPU usage, memory, etc.).
Press q to quit.
If you prefer a nicer interface, install htop:

sudo apt-get update
sudo apt-get install htop
htop

Press F10 or q to quit htop

## Killing a Process
If a process is stuck or unresponsive, you can kill it:
- kill <PID>
<PID> is the Process ID you see in ps aux or top.

If it won’t die, try a stronger signal:
- kill -9 <PID>
Use this carefully, as it force-kills the process.

