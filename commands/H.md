# H Commands (Termux Edition)

Commands starting with the letter **H**.

---

## `head`

**Description:**  
Displays the **first few lines of a file** (by default the first 10 lines).

**Use Case:**  
Quickly previewing the beginning of large log files or datasets without opening the entire file.

### Example

```bash
head logfile.txt
```

**Output (Snippet)**

```
[INFO] Server started
[INFO] Loading modules
[INFO] Listening on port 8080
```

Example with custom number of lines:

```bash
head -n 5 logfile.txt
```

---

## `history`

**Description:**  
Displays the list of **previously executed commands** in the terminal.

**Use Case:**  
Re-running previous commands, auditing what commands were executed, or debugging shell usage.

### Example

```bash
history
```

**Output (Snippet)**

```
1  pkg update
2  pkg install git
3  ls -la
4  cd projects
```

Example: Run a command from history

```bash
!3
```

---

## `hostname`

**Description:**  
Displays or sets the **system's host name**.

**Use Case:**  
Checking the device hostname or identifying systems in network environments.

### Example

```bash
hostname
```

**Output**

```
localhost
```

---

## `host`

**Description:**  
A **DNS lookup utility** used to find the IP address of a domain name.

**Use Case:**  
Checking domain DNS records or verifying connectivity to websites.

> Note: You may need to install it first.

```bash
pkg install dnsutils
```

### Example

```bash
host google.com
```

**Output (Snippet)**

```
google.com has address 142.250.183.206
```

---

## `htop`

**Description:**  
An **interactive system monitoring tool** that displays CPU usage, memory usage, and running processes.

**Use Case:**  
Monitoring system performance and managing running processes.

> Install if not available:

```bash
pkg install htop
```

### Example

```bash
htop
```

**Output**

```
Interactive process viewer showing CPU, memory, and running tasks.
```

---

## `hexdump`

**Description:**  
Displays the **binary contents of a file in hexadecimal format**.

**Use Case:**  
Inspecting binary files, debugging corrupted files, or analyzing file formats.

### Example

```bash
hexdump file.bin
```

**Output (Snippet)**

```
0000000 8950 4e47 0d0a 1a0a
0000010 0000 000d 4948 4452
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
