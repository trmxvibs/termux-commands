# W Commands (Termux Edition)

Commands starting with the letter **W**.

---

## `who`

**Description:**  
Displays information about **users currently logged into the system**.

**Use Case:**  
Checking active user sessions on multi-user systems.

### Example

```bash
who
```

**Output**

```
user   pts/0   2026-03-10 20:45
```

> Note: In Termux this usually shows limited information because Android typically runs a single user session.

---

## `whoami`

**Description:**  
Displays the **username of the current user**.

**Use Case:**  
Verifying which user account is currently executing commands or scripts.

### Example

```bash
whoami
```

**Output**

```
u0_a123
```

---

## `watch`

**Description:**  
Runs a command **repeatedly at fixed intervals** and displays the output.

**Use Case:**  
Monitoring system activity such as processes, memory usage, or directory changes.

### Example

```bash
watch ls
```

**Output**

```
Every 2.0s: ls

file1.txt
file2.txt
script.sh
```

Run command every 5 seconds:

```bash
watch -n 5 df -h
```

---

## `wc`

**Description:**  
Short for **word count**. It counts the number of **lines, words, and characters** in a file.

**Use Case:**  
Analyzing text files, logs, or datasets.

### Example

```bash
wc file.txt
```

**Output**

```
10  45  320 file.txt
```

Meaning:

```
10 → lines
45 → words
320 → characters
```

Count only lines:

```bash
wc -l file.txt
```

---

## `wget`

**Description:**  
A command-line tool used to **download files from the internet**.

**Use Case:**  
Downloading scripts, tools, or datasets directly from URLs.

### Example

```bash
wget https://example.com/file.zip
```

**Output (Snippet)**

```
Resolving example.com...
Connecting to example.com...
Saving to: 'file.zip'
```

---

## `whereis`

**Description:**  
Locates the **binary, source, and manual page files** for a command.

**Use Case:**  
Finding where a command is installed on the system.

### Example

```bash
whereis python
```

**Output**

```
python: /data/data/com.termux/files/usr/bin/python
```

---

## `which`

**Description:**  
Displays the **full path of the command executable** that will run when you type a command.

**Use Case:**  
Identifying which version of a command is being executed.

### Example

```bash
which python
```

**Output**

```
/data/data/com.termux/files/usr/bin/python
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
