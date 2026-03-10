# Networking Commands

<img width="3999" height="2140" alt="image" src="https://github.com/user-attachments/assets/2801913f-5d36-4c56-b7fe-fe9a68a91c3c" />

# Networking Commands

A collection of common **networking commands available in Termux/Linux** for diagnostics, connectivity testing, and network management.

---

## `arp`

Display or modify the **ARP (Address Resolution Protocol) cache**.

### Example

```bash
arp -a
```

---

## `curl`

Transfer data from or to a server using protocols such as **HTTP, HTTPS, and FTP**.

### Example

```bash
curl -I https://google.com
```

---

## `dig`

DNS lookup utility used to query DNS servers for domain information.

> Install if needed

```bash
pkg install dnsutils
```

### Example

```bash
dig google.com
```

---

## `ftp`

File Transfer Protocol client used to transfer files between machines.

### Example

```bash
ftp 192.168.1.50
```

---

## `host`

Perform DNS lookups to convert domain names into IP addresses.

### Example

```bash
host termux.dev
```

---

## `ifconfig`

Display or configure **network interfaces**.

> Mostly replaced by the `ip` command but still widely used.

### Example

```bash
ifconfig
```

---

## `ip`

Show or manipulate routing, network interfaces, and addresses.

### Example

```bash
ip a
```

---

## `lsof`

List open files. When used with `-i`, it shows **active network connections**.

### Example

```bash
lsof -i
```

---

## `mtr`

Network diagnostic tool combining **ping and traceroute**.

### Example

```bash
mtr google.com
```

---

## `nc` (Netcat)

A versatile networking utility used for **reading and writing network connections**.

### Example

```bash
nc -l -p 8080
```

---

## `netstat`

Display network connections, routing tables, and interface statistics.

### Example

```bash
netstat -tulpn
```

---

## `nmap`

Network exploration and **port scanning tool**.

### Example

```bash
nmap 192.168.1.1
```

---

## `nslookup`

Query DNS servers to find **IP addresses or domain information**.

### Example

```bash
nslookup github.com
```

---

## `ping`

Send ICMP packets to test **network connectivity**.

### Example

```bash
ping google.com
```

---

## `route`

Display or modify the **IP routing table**.

### Example

```bash
route -n
```

---

## `scp`

Securely copy files between machines using **SSH**.

### Example

```bash
scp file.txt user@192.168.1.10:/path/to/destination/
```

---

## `ss`

Display socket statistics. A modern alternative to `netstat`.

### Example

```bash
ss -tulw
```

---

## `ssh`

Secure Shell used to **connect to remote systems**.

### Example

```bash
ssh user@192.168.1.10 -p 8022
```

---

## `tcpdump`

Packet analyzer used to **capture network traffic**.

### Example

```bash
tcpdump -i wlan0
```

---

## `termux-wifi-connectioninfo`

(Termux specific)

Displays information about the current **Wi-Fi connection**.

> Requires `termux-api`

### Example

```bash
termux-wifi-connectioninfo
```

---

## `traceroute`

Shows the path packets take to reach a host.

### Example

```bash
traceroute google.com
```

---

## `vnstat`

Console-based **network traffic monitor**.

### Example

```bash
vnstat -i wlan0
```

---

## `wget`

Download files from the internet.

### Example

```bash
wget https://example.com/file.zip
```

---

## `whois`

Retrieve **domain registration information**.

### Example

```bash
whois github.com
```

---
