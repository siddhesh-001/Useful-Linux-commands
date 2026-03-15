---

Disclaimer

This repository is for educational purposes only. The commands provided here should be used responsibly in environments where you have proper authorization.

---

# 🐧 Linux Basic Commands Cheat Sheet

`< >` indicates user input.

---

##  Navigation

| Command | Description |
|--------|-------------|
| `pwd` | Show current directory |
| `ls` | List files |
| `ls -la` | List detailed files including hidden |
| `cd <folder>` | Enter directory |
| `cd ..` | Go back one directory |
| `cd ~` | Go to home directory |
| `clear` | Clear terminal screen |

---

## 📄 File Viewing

| Command | Description |
|--------|-------------|
| `cat <file>` | Print file contents |
| `less <file>` | View large files safely |
| `head <file>` | Show first 10 lines |
| `tail <file>` | Show last 10 lines |
| `tail -f <log_file>` | Monitor logs in real time |


---

##  File Management

| Command | Description |
|--------|-------------|
| `touch <file>` | Create empty file |
| `mkdir <folder_name>` | Create directory |
| `cp <source> <destination>` | Copy file |
| `cp -r <source_dir> <destination_dir>` | Copy directory |
| `mv <old_name> <new_name>` | Rename or move file |
| `rm <file>` | Delete file |
| `rm -r <folder>` | Delete directory |
| `echo "<text>"` | Print text |
| `nano <file>` | Edit file in terminal |

⚠️ Dangerous command:

```bash
rm -rf /
```

---

##  Searching & Text Processing

| Command | Description |
|--------|-------------|
| `grep <word> <file>` | Search text in file |
| `grep -r <word> <directory>` | Recursive search |
| `grep "<text>" <log_file>` | Search log entries |
| `find / -name <file>` | Find file by name |
| `find / -perm -4000` | Find SUID binaries |
| `find / -type f -name "*.conf"` | Find configuration files |

---

##  Networking

| Command | Description |
|--------|-------------|
| `ip a` | Show IP address |
| `ping <host>` | Test connectivity |
| `netstat -tuln` | Show open ports |
| `ss -tuln` | Faster netstat alternative |

---

##  Permissions

| Command | Description |
|--------|-------------|
| `ls -l` | Show file permissions |
| `chmod <permissions> <file>` | Change permissions |
| `chmod +x <script.sh>` | Make script executable |
| `chown <user> <file>` | Change file owner |

Permission values:

| Number | Meaning |
|------|---------|
| 7 | Read + Write + Execute |
| 6 | Read + Write |
| 5 | Read + Execute |
| 4 | Read Only |

---

##  Process Monitoring

| Command | Description |
|--------|-------------|
| `ps aux` | Show running processes |
| `top` | Real-time system monitoring |

---

##  Downloading Files

| Command | Description |
|--------|-------------|
| `wget <URL>` | Download file |
| `curl <URL>` | Fetch webpage |
| `curl -O <URL>` | Download file |

---

##  User & Privileges

| Command | Description |
|--------|-------------|
| `whoami` | Show current user |
| `id` | Show user and group IDs |
| `sudo <command>` | Run command as root |
| `sudo -l` | Show allowed sudo commands |

---

##  Help & History

| Command | Description |
|--------|-------------|
| `history` | Show command history |
| `man <command>` | Show manual page |
| `<command> --help` | Quick help |

---

##  Important Log Files (Security)

| File | Description |
|------|-------------|
| `/var/log/auth.log` | Login attempts |
| `/var/log/syslog` | System logs |
| `/var/log/apache2/access.log` | Web server access logs |
| `/var/log/apache2/error.log` | Web server error  |
