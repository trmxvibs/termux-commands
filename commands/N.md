# N Commands (Termux Edition)

Commands starting with the letter **N**.

---

## `nano`

**Description:**  
A simple and beginner-friendly **terminal text editor**.

**Use Case:**  
Editing configuration files, writing scripts, or quickly modifying text files directly from the terminal.

### Example

```bash
nano script.sh
```

**Output**

```
(The Nano text editor opens allowing you to edit the file.)
```

Common Nano shortcuts:

```
Ctrl + O → Save file
Ctrl + X → Exit editor
Ctrl + K → Cut line
Ctrl + U → Paste line
```

---

## `netstat`

**Description:**  
Displays **network connections, routing tables, and interface statistics**.

**Use Case:**  
Checking which ports are open or which programs are using network connections.

> Install if not available:

```bash
pkg install net-tools
```

### Example

```bash
netstat -tuln
```

**Output (Snippet)**

```
Proto Recv-Q Send-Q Local Address   Foreign Address State
tcp        0      0 0.0.0.0:8080    0.0.0.0:*       LISTEN
```

---

## `nice`

**Description:**  
Runs a program with a **modified CPU scheduling priority**.

**Use Case:**  
Running heavy programs with lower priority so they don't slow down the system.

### Example

```bash
nice -n 10 python heavy_script.py
```

**Output**

```
(The script runs with reduced CPU priority.)
```

---

## `nl`

**Description:**  
Numbers the lines of a file.

**Use Case:**  
Adding line numbers when reviewing scripts or logs.

### Example

```bash
nl notes.txt
```

**Output**

```
1  Install Termux
2  Setup storage
3  Install packages
```

---

## `nohup`

**Description:**  
Runs a command that **continues running even after the terminal session is closed**.

**Use Case:**  
Running long-running scripts or servers that should not stop when the terminal exits.

### Example

```bash
nohup python server.py &
```

**Output**

```
nohup: ignoring input and appending output to 'nohup.out'
```

---

## `nproc`

**Description:**  
Displays the **number of available CPU cores**.

**Use Case:**  
Determining how many CPU cores are available for compiling software or running parallel tasks.

### Example

```bash
nproc
```

**Output**

```
8
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
