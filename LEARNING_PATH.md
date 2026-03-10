# Termux Learning Path

This guide provides a structured roadmap to learn **Termux and Linux commands from beginner to advanced level**.

The goal is to help users gradually build practical skills in:

- Linux terminal usage
- Android file management
- Automation & scripting
- Networking & server hosting
- Security tools
- Mobile development environments

---

# Stage 0 — Initial Setup

**Goal:** Prepare your Termux environment for daily use.

### Key Concepts

- Updating repositories
- Granting storage permissions

### Commands to Learn

| Command | Purpose |
|------|------|
| `pkg update && pkg upgrade` | Update all installed packages |
| `termux-setup-storage` | Grant Termux access to phone storage |

### Example Workflow

```bash
pkg update && pkg upgrade -y
termux-setup-storage
cd ~/storage/downloads
ls
```

---

# Stage 1 — Beginner (Terminal Basics)

**Goal:** Become comfortable navigating the terminal and managing directories.

### Commands to Learn

| Command | Purpose |
|------|------|
| `pwd` | Show current directory path |
| `ls` | List files and folders |
| `cd` | Change directory |
| `mkdir` | Create a new folder |
| `touch` | Create an empty file |
| `rm` | Delete files (`rm -r` for folders) |
| `cp` | Copy files |
| `mv` | Move or rename files |
| `clear` | Clear terminal screen |
| `history` | View previously typed commands |

### Real World Example

Creating a workspace for scripts.

```bash
mkdir my_scripts
cd my_scripts
touch bot.py
ls
pwd
```

---

# Stage 2 — File Reading & Editing

**Goal:** Learn how to view and edit text files from the terminal.

### Commands to Learn

| Command | Purpose |
|------|------|
| `cat` | Display entire file content |
| `less` | View file page by page |
| `head` | Show first lines |
| `tail` | Show last lines |
| `nano` | Beginner text editor |
| `vim` | Advanced text editor |

### Example Workflow

```bash
nano hello.sh
```

Inside nano:

```
Ctrl + O → Save
Ctrl + X → Exit
```

---

# Stage 3 — Archiving & Compression

**Goal:** Compress and extract files.

### Commands to Learn

| Command | Purpose |
|------|------|
| `tar` | Create/extract `.tar.gz` archives |
| `zip` | Compress files |
| `unzip` | Extract `.zip` files |

### Example

```bash
unzip project-master.zip
cd project-master
```

---

# Stage 4 — Permissions & Environment

**Goal:** Understand Linux permissions and variables.

### Commands

| Command | Purpose |
|------|------|
| `chmod` | Change file permissions |
| `whoami` | Show current user |
| `id` | Show user/group info |
| `env` | Show environment variables |
| `export` | Create environment variables |

### Example

```bash
chmod +x hello.sh
./hello.sh
```

---

# Stage 5 — Package Management

**Goal:** Install tools and programming languages.

### Commands

| Command | Purpose |
|------|------|
| `pkg search` | Search packages |
| `pkg install` | Install package |
| `pkg uninstall` | Remove package |
| `apt list --installed` | Show installed packages |
| `dpkg -i` | Install local `.deb` file |

### Example

```bash
pkg search python
pkg install python -y
python --version
```

---

# Stage 6 — Text Processing

**Goal:** Search and manipulate text efficiently.

### Commands

| Command | Purpose |
|------|------|
| `grep` | Search patterns |
| `awk` | Extract columns |
| `sed` | Replace text |
| `sort` | Sort lines |
| `uniq` | Remove duplicates |

### Example

```bash
grep "ERROR" server_log.txt
```

---

# Stage 7 — Networking

**Goal:** Learn connectivity and remote access.

### Commands

| Command | Purpose |
|------|------|
| `ping` | Test internet connection |
| `curl` | Fetch web/API data |
| `wget` | Download files |
| `ifconfig` / `ip a` | Show IP address |
| `ssh` | Remote login |
| `scp` | Secure file transfer |

### Example

```bash
ifconfig
ping google.com
```

---

# Stage 8 — System Monitoring

**Goal:** Monitor system resources.

### Commands

| Command | Purpose |
|------|------|
| `ps` | Show running processes |
| `htop` | Process monitor |
| `df -h` | Disk usage |
| `du -sh` | Folder size |
| `termux-wake-lock` | Prevent phone sleep |

### Example

```bash
pkg install htop
htop
```

---

# Stage 9 — Automation & Scripting

**Goal:** Automate tasks using Bash scripts.

### Example Script

```bash
#!/bin/bash

echo "Starting Termux Maintenance..."

termux-wake-lock

pkg update -y
pkg upgrade -y
pkg clean

termux-wake-unlock

echo "System successfully updated!"
```

Run script:

```bash
chmod +x update_all.sh
./update_all.sh
```

---

# Stage 10 — Development Environment

**Goal:** Turn Termux into a development machine.

### Commands

| Command | Purpose |
|------|------|
| `git` | Version control |
| `termux-api` | Access Android hardware |

### Example

```bash
pkg install git termux-api
git clone https://github.com/your-username/project.git
termux-battery-status
```

---

# Stage 11 — Advanced & Security Tools

⚠ Use only on **your own network or for legal research purposes**.

### Tools

- `nmap` → network scanner
- `metasploit` → exploitation framework
- `tshark` → network analyzer
- `sqlmap` → database testing

### Example

```bash
pkg install nmap
nmap -sV 192.168.1.1
```

---

# Recommended Learning Strategy

### Daily Practice

- Learn **3–5 commands per day**
- Practice typing commands yourself
- Experiment with flags and options

### Get Help

```bash
man ls
```

or

```bash
ls --help
```
