# T Commands (Termux Edition)

Commands starting with the letter **T**.

---

## `tar`

**Description:**  
Short for **Tape Archive**. It is used to **create, extract, and manage archive files**.

**Use Case:**  
Bundling multiple files into a single archive or extracting downloaded `.tar`, `.tar.gz`, or `.tar.xz` files.

### Example

Create archive:

```bash
tar -cvf archive.tar folder/
```

**Output (Snippet)**

```
folder/
folder/file1.txt
folder/file2.txt
```

Extract archive:

```bash
tar -xvf archive.tar
```

Extract compressed archive:

```bash
tar -xzf archive.tar.gz
```

---

## `top`

**Description:**  
Displays **real-time system processes**, CPU usage, and memory usage.

**Use Case:**  
Monitoring system performance and identifying resource-heavy programs.

### Example

```bash
top
```

**Output (Snippet)**

```
PID USER     PR  NI    VIRT    RES  %CPU %MEM     TIME+ COMMAND
1234 user     20   0  350000  25000   5.2  1.3   0:01.22 python
```

Press `q` to quit.

---

## `touch`

**Description:**  
Creates a **new empty file** or updates the timestamp of an existing file.

**Use Case:**  
Quickly creating placeholder files or updating modification times.

### Example

```bash
touch notes.txt
```

**Output**

```
(A new file named notes.txt is created if it doesn't exist.)
```

---

## `tee`

**Description:**  
Reads input and **writes it to both the terminal and a file simultaneously**.

**Use Case:**  
Saving command output while still viewing it on the screen.

### Example

```bash
echo "Hello Termux" | tee output.txt
```

**Output**

```
Hello Termux
```

Append to file:

```bash
echo "New line" | tee -a output.txt
```

---

## `time`

**Description:**  
Measures how long a command takes to execute.

**Use Case:**  
Benchmarking scripts or measuring program performance.

### Example

```bash
time ls
```

**Output**

```
real    0m0.012s
user    0m0.005s
sys     0m0.003s
```

---

## `tr`

**Description:**  
Short for **translate**. It replaces or deletes characters from input text.

**Use Case:**  
Text processing such as converting lowercase letters to uppercase.

### Example

```bash
echo "termux" | tr 'a-z' 'A-Z'
```

**Output**

```
TERMUX
```

Example removing numbers:

```bash
echo "hello123" | tr -d '0-9'
```

---

## `tree`

**Description:**  
Displays directories in a **tree-like structure**.

**Use Case:**  
Visualizing folder hierarchies.

> Install if not available:

```bash
pkg install tree
```

### Example

```bash
tree
```

**Output**

```
.
├── script.sh
├── projects
│   ├── app.py
│   └── README.md
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
