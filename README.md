# Linux Commands Cheat Sheet (Cybersecurity Basics)

--------------------------------------------------
NAVIGATION
--------------------------------------------------
pwd                 Show current directory
ls                  List files
ls -la              List all files (including hidden)
cd folder           Enter directory
cd ..               Go back one directory
cd ~                Go to home directory

--------------------------------------------------
FILE VIEWING
--------------------------------------------------
cat file.txt        Print file contents
less file.txt       View large files safely
head file.txt       Show first 10 lines
tail file.txt       Show last 10 lines
tail -f file.log    Monitor log file in real time

--------------------------------------------------
FILE MANAGEMENT
--------------------------------------------------
cp file1 file2      Copy file
cp -r dir1 dir2     Copy directory
mv old new          Rename or move file
rm file.txt         Delete file
rm -r folder        Delete directory

WARNING:
rm -rf /            Dangerous command (can delete system)

--------------------------------------------------
SEARCHING
--------------------------------------------------
find / -name file.txt                Find file by name
find / -perm -4000 2>/dev/null       Find SUID binaries
grep word file.txt                   Search text in file
grep -r word .                       Recursive search
grep "failed" /var/log/auth.log      Search log entries

--------------------------------------------------
NETWORKING
--------------------------------------------------
ip a                Show IP address
ping host           Test connectivity
netstat -tuln       Show open ports
ss -tuln            Faster netstat alternative

--------------------------------------------------
PERMISSIONS
--------------------------------------------------
ls -l               Show file permissions
chmod 755 file      Change permissions
chown user file     Change file owner

Permission Numbers:
7 = read + write + execute
6 = read + write
5 = read + execute
4 = read only

--------------------------------------------------
PROCESS MONITORING
--------------------------------------------------
ps aux              Show running processes
top                 Real-time system monitor

--------------------------------------------------
DOWNLOAD FILES
--------------------------------------------------
wget URL            Download file
curl URL            Fetch webpage
curl -O URL         Download file with curl

--------------------------------------------------
USEFUL SECURITY COMMAND
--------------------------------------------------
history             Show previously executed commands

--------------------------------------------------
PRACTICE
--------------------------------------------------
pwd
ls -la
cd /var/log
tail syslog
