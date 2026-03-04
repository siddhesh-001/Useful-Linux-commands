# 🐧 Linux Commands Cheat Sheet (Cybersecurity Basics)

A quick reference for essential Linux commands commonly used in cybersecurity, penetration testing, and system administration.

---

# 📂 Navigation

| Command | Description |
|--------|-------------|
| `pwd` | Show current directory |
| `ls` | List files |
| `ls -la` | List all files including hidden ones |
| `cd folder` | Enter directory |
| `cd ..` | Go back one directory |
| `cd ~` | Go to home directory |


---

# 📄 File Viewing

| Command | Description |
|--------|-------------|
| `cat file.txt` | Print file contents |
| `less file.txt` | View large files safely |
| `head file.txt` | Show first 10 lines |
| `tail file.txt` | Show last 10 lines |
| `tail -f log.txt` | Monitor logs in real time |

Example:

```bash
tail -f /var/log/syslog
```

---

# 📁 File Management

| Command | Description |
|--------|-------------|
| `cp file1 file2` | Copy file |
| `cp -r dir1 dir2` | Copy directory |
| `mv old new` | Rename or move file |
| `rm file.txt` | Delete file |
| `rm -r folder` | Delete directory |

⚠️ Dangerous command:

```bash
rm -rf /
```

This can delete the entire system.

---

# 🔍 Searching

| Command | Description |
|--------|-------------|
| `find / -name file.txt` | Find file by name |
| `find / -perm -4000 2>/dev/null` | Find SUID binaries |
| `grep word file.txt` | Search text in file |
| `grep -r word .` | Recursive search |
| `grep "failed" /var/log/auth.log` | Search log entries |

Example:

```bash
grep password config.txt
```

---

# 🌐 Networking

| Command | Description |
|--------|-------------|
| `ip a` | Show IP address |
| `ping host` | Test connectivity |
| `netstat -tuln` | Show open ports |
| `ss -tuln` | Faster netstat alternative |

Example:

```bash
ip a
ping google.com
```

---

# 🔐 Permissions

| Command | Description |
|--------|-------------|
| `ls -l` | Show file permissions |
| `chmod 755 file` | Change file permissions |
| `chown user file` | Change file owner |

Permission values:

| Number | Meaning |
|------|---------|
| 7 | Read + Write + Execute |
| 6 | Read + Write |
| 5 | Read + Execute |
| 4 | Read Only |

---

# ⚙️ Process Monitoring

| Command | Description |
|--------|-------------|
| `ps aux` | Show running processes |
| `top` | Real-time system monitoring |

Example:

```bash
ps aux
top
```

---

#  Downloading Files

| Command | Description |
|--------|-------------|
| `wget URL` | Download file |
| `curl URL` | Fetch webpage |
| `curl -O URL` | Download file |

Example:

```bash
wget https://example.com/file.txt
```

---

#  Useful Security Command

| Command | Description |
|--------|-------------|
| `history` | Show command history |

Attackers sometimes discover passwords or tokens in command history.


