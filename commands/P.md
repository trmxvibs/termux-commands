# P Commands (Termux Edition)

Commands starting with the letter **P**.

---

## `pwd`

**Description:**  
Stands for **"print working directory"**. It shows the current directory path where you are currently located in the terminal.

**Use Case:**  
Confirming your current location in the filesystem, especially when navigating multiple directories.

### Example

```bash
pwd
```

**Output**

```
/data/data/com.termux/files/home
```

---

## `ping`

**Description:**  
Sends network packets to a host to check **connectivity and response time**.

**Use Case:**  
Testing whether a website or server is reachable from your device.

### Example

```bash
ping google.com
```

**Output (Snippet)**

```
PING google.com (142.250.183.206): 56 data bytes
64 bytes from 142.250.183.206: icmp_seq=0 ttl=118 time=24.5 ms
```

Stop ping with:

```
Ctrl + C
```

---

## `ps`

**Description:**  
Displays information about **currently running processes**.

**Use Case:**  
Checking which programs are running in the system.

### Example

```bash
ps
```

**Output (Snippet)**

```
USER       PID  PPID  VSZ   RSS  WCHAN    PC  NAME
u0_a123   1345  1234  548M  45M  futex_wait 0  python
```

Example with more details:

```bash
ps aux
```

---

## `passwd`

**Description:**  
Changes the **password for a user account**.

**Use Case:**  
Updating account security credentials.

### Example

```bash
passwd
```

**Output**

```
Changing password for user
New password:
Retype new password:
```

> Note: In Termux this command is rarely used because it runs in a single-user environment.

---

## `pgrep`

**Description:**  
Searches for processes by **name or pattern** and returns their process IDs (PID).

**Use Case:**  
Quickly finding the PID of a running program.

### Example

```bash
pgrep python
```

**Output**

```
2451
```

---

## `pkill`

**Description:**  
Kills processes **based on name or pattern** instead of PID.

**Use Case:**  
Stopping running programs without needing to find their PID manually.

### Example

```bash
pkill python
```

**Output**

```
(All running python processes are terminated.)
```

---

## `python`

**Description:**  
Runs the **Python programming language interpreter**.

**Use Case:**  
Executing Python scripts, testing code, or running Python-based tools.

### Example

```bash
python
```

**Output**

```
Python 3.x.x (default, ...)
>>> 
```

Example running a script:

```bash
python script.py
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
