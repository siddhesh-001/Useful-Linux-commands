# 🐧 Basic Linux Commands Cheat Sheet

A beginner-friendly **Linux command reference** designed for learning terminal navigation and building a strong foundation for **cybersecurity and system administration**.

Many cybersecurity tools and labs run on Linux distributions such as **Kali Linux** and **Ubuntu**, so understanding basic terminal commands is essential.

---

# 📂 File System Basics

Linux organizes files in a **hierarchical structure** that starts at the root directory.

Example path:


/home/user/Documents


Explanation:

| Component | Meaning |
|----------|--------|
| `/` | Root directory (top of the system) |
| `home` | Directory where user accounts are stored |
| `user` | Individual user folder |

---

# 📋 Essential Linux Commands

| Command | Purpose |
|-------|--------|
| `pwd` | Show current directory |
| `ls` | List files and folders |
| `cd` | Change directory |
| `mkdir` | Create a new folder |
| `touch` | Create a file |
| `cat` | View file content |
| `cp` | Copy files |
| `mv` | Move or rename files |
| `rm` | Delete files |
| `whoami` | Show current user |

---

# 1️⃣ Print Working Directory (`pwd`)

Displays the **current directory path** you are working in.

```bash
pwd

Example output:

/home/wick

[!NOTE]
This command helps you confirm where you are in the file system, especially when navigating multiple directories.

2️⃣ List Files (ls)

Shows files and directories inside the current folder.

ls

Example output:

Documents  Downloads  notes.txt
Useful Options
Command	Description
ls -l	Detailed file information
ls -a	Show hidden files

Example:

ls -la

[!TIP]
Hidden files start with a dot (.) and often store configuration data.

3️⃣ Change Directory (cd)

Used to move between directories.

Move into a folder
cd Documents
Move back one directory
cd ..
Go to the home directory
cd ~

Example navigation:

/home/wick → Documents → Projects

Commands used:

cd Documents
cd Projects
4️⃣ Create a Directory (mkdir)

Creates a new folder.

mkdir cyberlab

Verify creation:

ls

Example output:

cyberlab
5️⃣ Create a File (touch)

Creates an empty file.

touch notes.txt

Verify:

ls

Example output:

notes.txt
6️⃣ View File Content (cat)

Displays the contents of a file.

cat notes.txt

Example output:

Linux commands practice

Common use cases:

Reading configuration files

Viewing logs

Inspecting scripts

7️⃣ Copy Files (cp)

Creates a copy of a file.

cp notes.txt backup.txt

Result:

notes.txt
backup.txt
8️⃣ Move or Rename Files (mv)
Rename a file
mv notes.txt linux_notes.txt
Move a file to another folder
mv linux_notes.txt Documents/
9️⃣ Remove Files (rm)

Deletes files or directories.

Delete a file
rm file.txt
Delete a folder
rm -r foldername

[!WARNING]
Files deleted using rm cannot be recovered easily. There is no recycle bin in the terminal.

🔎 Check Current User (whoami)

Displays the username currently logged into the system.

whoami

Example output:

wick

This command is useful in cybersecurity when checking user privileges and access levels.

🧪 Beginner Practice Exercise

Try these commands in your Linux terminal.

mkdir cyberlab
cd cyberlab
touch notes.txt
ls
cat notes.txt

This exercise demonstrates:

Step	Action
1	Create a directory
2	Navigate into the directory
3	Create a file
4	List files
5	View file content
⚠️ Common Beginner Mistakes
1️⃣ Missing spaces in commands

Incorrect:

cdDocuments

Correct:

cd Documents
2️⃣ Case sensitivity

Linux distinguishes uppercase and lowercase letters.

Documents ≠ documents
3️⃣ Dangerous deletion commands
rm -rf

This command can delete entire directories recursively without confirmation.

[!WARNING]
Always double-check before using destructive commands.

📚 Commands to Memorize First

Focus on mastering these core commands:

pwd
ls
cd
mkdir
touch
cat
cp
mv
rm
whoami

Understanding these commands will allow you to perform most beginner Linux tasks efficiently.
