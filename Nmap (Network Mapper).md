#  Nmap Cheat Sheet (Network Mappinging)

`< >` indicates user input.

---

##  Host Discovery

| Command | Description |
|--------|-------------|
| `nmap -sn <network>` | Ping scan (discover live hosts without port scan) |
| `nmap -Pn <target>` | Skip host discovery and scan host directly |

Example:

```bash
nmap -sn 192.168.1.0/24
```

---

##  Basic Scanning

| Command | Description |
|--------|-------------|
| `nmap <target_ip>` | Basic scan of a target |
| `nmap <target1> <target2>` | Scan multiple targets |
| `nmap <network>/24` | Scan entire subnet |
| `nmap -p <port> <target>` | Scan specific port |
| `nmap -p- <target>` | Scan all 65535 ports |
| `nmap -F <target>` | Fast scan (top 100 ports) |
| `nmap --open <target>` | Show only open ports |

Example:

```bash
nmap 192.168.1.10
```

---

##  Scan Types

| Command | Description |
|--------|-------------|
| `nmap -sS <target>` | TCP SYN scan (stealth scan) |
| `nmap -sT <target>` | TCP connect scan |
| `nmap -sU <target>` | UDP scan |
| `nmap -sA <target>` | ACK scan |
| `nmap -sN <target>` | Null scan |

Example:

```bash
nmap -sS 192.168.1.10
```

---

##  Service & OS Detection

| Command | Description |
|--------|-------------|
| `nmap -sV <target>` | Detect service versions |
| `nmap -O <target>` | Detect operating system |
| `nmap -A <target>` | Aggressive scan (OS + version + scripts) |
| `nmap -sC <target>` | Run default Nmap scripts |

Example:

```bash
nmap -sV 192.168.1.10
```

---

##  Scan Speed

| Command | Description |
|--------|-------------|
| `nmap -T0 <target>` | Paranoid (very slow) |
| `nmap -T1 <target>` | Sneaky |
| `nmap -T2 <target>` | Polite |
| `nmap -T3 <target>` | Normal (default) |
| `nmap -T4 <target>` | Faster scan |
| `nmap -T5 <target>` | Insane (very fast) |

Example:

```bash
nmap -T4 192.168.1.10
```

---

##  Nmap Scripting Engine (NSE)

| Command | Description |
|--------|-------------|
| `nmap --script=vuln <target>` | Run vulnerability scripts |
| `nmap --script=safe <target>` | Run safe scripts |
| `nmap --script=http-enum <target>` | Enumerate web directories |
| `nmap --script=ftp-anon <target>` | Check anonymous FTP login |

Example:

```bash
nmap --script=vuln 192.168.1.10
```

---

##  Output & Verbosity

| Command | Description |
|--------|-------------|
| `nmap -v <target>` | Verbose output |
| `nmap -vv <target>` | Very verbose output |
| `nmap -oN <file> <target>` | Save output to file |
| `nmap -oA <name> <target>` | Save output in all formats |

Example:

```bash
nmap -oN scan.txt 192.168.1.10
```
