# S Commands (Termux Edition)

Commands starting with the letter **S**.

---

## `sed`

**Description:**  
Stream Editor used to **search, replace, filter, and transform text** in files or input streams.

**Use Case:**  
Automating text editing tasks such as replacing words in configuration files or logs.

### Example

```bash
sed 's/Termux/Linux/' file.txt
```

**Output**

```
(Lines from file.txt with "Termux" replaced by "Linux")
```

Replace text directly in file:

```bash
sed -i 's/old/new/g' file.txt
```

---

## `sort`

**Description:**  
Sorts lines of text files **alphabetically or numerically**.

**Use Case:**  
Organizing lists, logs, or datasets.

### Example

```bash
sort names.txt
```

**Output**

```
Alice
Bob
Charlie
```

Numeric sort:

```bash
sort -n numbers.txt
```

---

## `ssh`

**Description:**  
Secure Shell client used to **connect to remote servers securely**.

**Use Case:**  
Accessing remote machines, servers, or VPS instances from Termux.

### Example

```bash
ssh user@192.168.1.10
```

**Output**

```
user@192.168.1.10's password:
```

Example with port:

```bash
ssh -p 2222 user@server.com
```

---

## `scp`

**Description:**  
Secure Copy Protocol used to **transfer files between local and remote systems over SSH**.

**Use Case:**  
Uploading or downloading files securely from servers.

### Example

Upload file to server:

```bash
scp file.txt user@server:/home/user/
```

Download file from server:

```bash
scp user@server:/home/user/file.txt .
```

---

## `stat`

**Description:**  
Displays detailed **file or filesystem information**.

**Use Case:**  
Checking file size, permissions, timestamps, and metadata.

### Example

```bash
stat file.txt
```

**Output (Snippet)**

```
File: file.txt
Size: 245        Blocks: 8
Access: (0644/-rw-r--r--)
Modify: 2026-03-10
```

---

## `sleep`

**Description:**  
Pauses execution of a script or command for a specified time.

**Use Case:**  
Adding delays in shell scripts.

### Example

```bash
sleep 5
```

**Output**

```
(Command pauses for 5 seconds.)
```

Example in script:

```bash
echo "Starting..."
sleep 3
echo "Done"
```

---

## `screen`

**Description:**  
A terminal multiplexer that allows **multiple terminal sessions inside one window**.

**Use Case:**  
Running programs that should continue even after closing the terminal.

> Install if not available:

```bash
pkg install screen
```

### Example

```bash
screen
```

**Output**

```
(A new screen session starts.)
```

Detach session:

```
Ctrl + A then D
```

Reattach session:

```bash
screen -r
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
