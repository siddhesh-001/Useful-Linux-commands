#  Network Reconnaissance Cheat Sheet

`< >` indicates user input.

---

##  Host Discovery

| Command | Description |
|--------|-------------|
| `ping <host>` | Check if host is reachable |
| `nmap -sn <network>` | Discover live hosts in network |
| `arp -a` | Show devices on local network |

Example:

```bash
ping <target_ip>
```

---

##  Port Scanning

| Command | Description |
|--------|-------------|
| `nmap <target>` | Basic port scan |
| `nmap -p- <target>` | Scan all ports |
| `nmap -sS <target>` | Stealth SYN scan |
| `nc -zv <target> <port>` | Check if port is open |

Example:

```bash
nmap <target_ip>
```

---

##  DNS Enumeration

| Command | Description |
|--------|-------------|
| `dig <domain>` | Query DNS records |
| `nslookup <domain>` | DNS lookup |
| `host <domain>` | Resolve domain to IP |

Example:

```bash
dig <domain>
```

---

##  Network Information

| Command | Description |
|--------|-------------|
| `ip a` | Show network interfaces |
| `ip route` | Show routing table |
| `ss -tuln` | Show listening ports |
| `netstat -tuln` | Show open ports |

Example:

```bash
ip a
```

---

##  Network Path Analysis

| Command | Description |
|--------|-------------|
| `traceroute <host>` | Show network path to host |

Example:

```bash
traceroute <target_ip>
```

---

##  Web Requests & File Download

| Command | Description |
|--------|-------------|
| `curl <URL>` | Fetch webpage |
| `curl -I <URL>` | Show HTTP headers |
| `wget <URL>` | Download file |

Example:

```bash
curl -I <URL>
```

---

##  Packet Capture

| Command | Description |
|--------|-------------|
| `tcpdump -i <interface>` | Capture network packets |
| `tcpdump -i <interface> port <port>` | Capture traffic on specific port |

Example:

```bash
tcpdump -i eth0
```

---

##  Manual Network Connections

| Command | Description |
|--------|-------------|
| `nc <target> <port>` | Connect to service |
| `nc -lvnp <port>` | Start listener |

Example:

```bash
nc <target_ip> 80
```
