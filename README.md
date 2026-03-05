# 🐧 Linux Commands Cheat Sheet (Cybersecurity Basics)

```
+--------------------------------------+-----------------------------------------------+
| NAVIGATION                                                                   |
+--------------------------------------+-----------------------------------------------+
| pwd                                  | Show current directory                        |
| ls                                   | List files                                    |
| ls -la                               | List detailed files including hidden          |
| cd <folder>                          | Enter directory                               |
| cd ..                                | Go back one directory                         |
| cd ~                                 | Go to home directory                          |
| clear                                | Clear terminal screen                         |
+--------------------------------------+-----------------------------------------------+

+--------------------------------------+-----------------------------------------------+
| FILE VIEWING                                                                 |
+--------------------------------------+-----------------------------------------------+
| cat <file>                           | Print file contents                           |
| less <file>                          | View large files safely                       |
| head <file>                          | Show first 10 lines                           |
| tail <file>                          | Show last 10 lines                            |
| tail -f <log_file>                   | Monitor logs in real time                     |
+--------------------------------------+-----------------------------------------------+

+--------------------------------------+-----------------------------------------------+
| FILE MANAGEMENT                                                              |
+--------------------------------------+-----------------------------------------------+
| touch <file>                         | Create empty file                             |
| mkdir <folder_name>                  | Create directory                              |
| cp <source> <destination>            | Copy file                                     |
| cp -r <source_dir> <destination_dir> | Copy directory                                |
| mv <old_name> <new_name>             | Rename or move file                           |
| rm <file>                            | Delete file                                   |
| rm -r <folder>                       | Delete directory                              |
| echo "<text>"                        | Print text or write to file                   |
| nano <file>                          | Edit file in terminal                         |
+--------------------------------------+-----------------------------------------------+

⚠ Dangerous command:
rm -rf /
(Delete entire system if executed as root)

+--------------------------------------+-----------------------------------------------+
| SEARCHING & TEXT PROCESSING                                               |
+--------------------------------------+-----------------------------------------------+
| grep <word> <file>                   | Search text in file                           |
| grep -r <word> <directory>           | Recursive search                              |
| grep "<text>" <log_file>             | Search log entries                            |
| find / -name <file>                  | Find file by name                             |
| find / -perm -4000                   | Find SUID binaries                            |
| find / -type f -name "*.conf"        | Find configuration files                      |
+--------------------------------------+-----------------------------------------------+

+--------------------------------------+-----------------------------------------------+
| NETWORKING                                                                  |
+--------------------------------------+-----------------------------------------------+
| ip a                                 | Show IP address                               |
| ping <host>                           | Test connectivity                             |
| netstat -tuln                         | Show open ports                               |
| ss -tuln                              | Faster netstat alternative                    |
+--------------------------------------+-----------------------------------------------+

+--------------------------------------+-----------------------------------------------+
| PERMISSIONS                                                                 |
+--------------------------------------+-----------------------------------------------+
| ls -l                                | Show file permissions                         |
| chmod <permissions> <file>           | Change file permissions                       |
| chmod +x <script.sh>                 | Make script executable                        |
| chown <user> <file>                  | Change file owner                             |
+--------------------------------------+-----------------------------------------------+

Permission values:
7 = Read + Write + Execute
6 = Read + Write
5 = Read + Execute
4 = Read Only

+--------------------------------------+-----------------------------------------------+
| PROCESS MONITORING                                                         |
+--------------------------------------+-----------------------------------------------+
| ps aux                               | Show running processes                        |
| top                                  | Real-time system monitoring                   |
+--------------------------------------+-----------------------------------------------+

+--------------------------------------+-----------------------------------------------+
| DOWNLOADING FILES                                                          |
+--------------------------------------+-----------------------------------------------+
| wget <URL>                           | Download file                                 |
| curl <URL>                           | Fetch webpage                                 |
| curl -O <URL>                        | Download file                                 |
+--------------------------------------+-----------------------------------------------+

+--------------------------------------+-----------------------------------------------+
| USER & PRIVILEGES                                                          |
+--------------------------------------+-----------------------------------------------+
| whoami                               | Show current user                             |
| id                                   | Show user and group IDs                       |
| sudo <command>                       | Run command as root                           |
| sudo -l                              | Show allowed sudo commands                    |
+--------------------------------------+-----------------------------------------------+

+--------------------------------------+-----------------------------------------------+
| HELP & HISTORY                                                             |
+--------------------------------------+-----------------------------------------------+
| history                              | Show command history                          |
| man <command>                        | Show manual page                              |
| <command> --help                     | Show quick help                               |
+--------------------------------------+-----------------------------------------------+

+--------------------------------------+-----------------------------------------------+
| IMPORTANT LOG FILES (SECURITY)                                            |
+--------------------------------------+-----------------------------------------------+
| /var/log/auth.log                    | Login attempts                                |
| /var/log/syslog                      | System logs                                   |
| /var/log/apache2/access.log          | Web server access logs                        |
| /var/log/apache2/error.log           | Web server error logs                         |
+--------------------------------------+-----------------------------------------------+
```
