# Termux Learning Path

This guide provides a structured roadmap to learn Termux and Linux commands from **beginner to advanced level**.

The goal is to help users gradually build practical skills in:

- Linux terminal usage
- File management
- Automation
- Networking
- Security tools
- Development environments

---

# Stage 1 — Beginner (Terminal Basics)

Goal: Become comfortable navigating the terminal.

Key Concepts

- Directory navigation
- File creation
- Command syntax
- Terminal shortcuts

Commands to Learn

| Command | Purpose |
|------|------|
| pwd | show current directory |
| ls | list files |
| cd | change directory |
| mkdir | create folder |
| touch | create file |
| rm | delete files |
| cp | copy files |
| mv | move files |
| clear | clear terminal |
| history | command history |

Example Workflow

```bash
mkdir project
cd project
touch index.html
ls
pwd
```

Real World Example

Creating a small project folder to store scripts or notes.

---

# Stage 2 — File Reading & Editing

Goal: Learn how to view and edit files.

Commands

| Command | Purpose |
|------|------|
| cat | display file |
| less | view file page by page |
| head | first lines of file |
| tail | last lines |
| nano | basic editor |
| vim | advanced editor |

Example

```bash
nano script.sh
```

Example Script

```bash
#!/bin/bash
echo "Hello from Termux"
```

Run it

```bash
bash script.sh
```

---

# Stage 3 — Permissions & Environment

Goal: Understand Linux file permissions.

Commands

| Command | Purpose |
|------|------|
| chmod | change permissions |
| chown | change owner |
| whoami | current user |
| id | user information |
| env | environment variables |

Example

```bash
chmod +x script.sh
```

Now run directly

```bash
./script.sh
```

Real World Example

Running automation scripts.

---

# Stage 4 — Package Management

Goal: Install tools and programming languages.

Commands

| Command | Purpose |
|------|------|
| pkg | Termux package manager |
| apt | Debian package manager |
| dpkg | low level package tool |

Example

```bash
pkg update
pkg upgrade
pkg install python
```

Example

```bash
python
```

You now have a Python environment on your phone.

---

# Stage 5 — Text Processing

Goal: Process logs and large datasets.

Commands

| Command | Purpose |
|------|------|
| grep | search text |
| awk | data extraction |
| sed | text editing |
| cut | column extraction |
| sort | sort lines |
| uniq | remove duplicates |

Example

```bash
grep "error" log.txt
```

Example

```bash
cat users.txt | sort | uniq
```

Real World Example

Analyzing server logs.

---

# Stage 6 — Networking

Goal: Learn network diagnostics and remote access.

Commands

| Command | Purpose |
|------|------|
| ping | connectivity test |
| curl | API requests |
| wget | download files |
| ssh | remote login |
| scp | file transfer |
| netstat | network connections |
| nmap | network scanning |

Example

```bash
ping google.com
```

Example

```bash
ssh user@192.168.1.10 -p 8022
```

Real World Example

Accessing a home server from your phone.

---

# Stage 7 — System Monitoring

Goal: Monitor processes and system usage.

Commands

| Command | Purpose |
|------|------|
| ps | running processes |
| top | live process list |
| htop | advanced monitor |
| free | memory usage |
| df | disk usage |
| du | folder size |

Example

```bash
htop
```

Real World Example

Identify which process is consuming CPU.

---

# Stage 8 — Automation & Scripting

Goal: Automate tasks using Bash scripts.

Example Script

```bash
#!/bin/bash

echo "Updating system..."

pkg update
pkg upgrade -y

echo "System updated"
```

Save as

```
update.sh
```

Run

```bash
bash update.sh
```

---

# Stage 9 — Development Environment

Goal: Turn Termux into a development machine.

Install tools

```bash
pkg install git
pkg install nodejs
pkg install python
pkg install clang
```

Example

```bash
git clone https://github.com/user/project
```

Real World Example

Developing code directly from mobile.

---

# Stage 10 — Advanced Tools

Goal: Advanced networking and security tools.

Commands

| Command | Purpose |
|------|------|
| nmap | network scanner |
| hydra | brute force tool |
| sqlmap | SQL injection testing |
| metasploit | exploitation framework |

Example

```bash
nmap -sV 192.168.1.1
```

Important

Use tools **only for legal and educational purposes**.

---

# Recommended Learning Strategy

Daily practice:

1. Learn **5 commands per day**
2. Try real examples
3. Read command manuals

Example

```bash
man ls
```

or

```bash
ls --help
```

---

# Final Goal

By completing this learning path you will be able to:

- Use Linux terminal efficiently
- Automate tasks
- Manage servers
- Develop software
- Use advanced networking tools
- Master Termux environment
