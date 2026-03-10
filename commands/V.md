# V Commands (Termux Edition)

Commands starting with the letter **V**.

---

## `vi`

**Description:**  
A powerful **terminal-based text editor** used to create and edit files.

**Use Case:**  
Editing configuration files, scripts, or source code directly from the terminal.

### Example

```bash
vi script.sh
```

**Output**

```
(The vi editor opens the file for editing.)
```

Common `vi` commands:

```
i → insert mode
Esc → return to command mode
:w → save file
:q → quit editor
:wq → save and quit
```

---

## `vim`

**Description:**  
An advanced version of `vi` with additional features like **syntax highlighting, plugins, and better navigation**.

**Use Case:**  
Editing source code or configuration files efficiently.

> Install if not available:

```bash
pkg install vim
```

### Example

```bash
vim notes.txt
```

**Output**

```
(The Vim editor opens the file.)
```

Useful commands:

```
:help → open help
:w → save
:q → quit
:wq → save and quit
```

---

## `vmstat`

**Description:**  
Displays information about **system memory, processes, CPU usage, and I/O activity**.

**Use Case:**  
Monitoring system performance and diagnosing performance bottlenecks.

### Example

```bash
vmstat
```

**Output (Snippet)**

```
procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st
 1  0      0  52324  10244  30012    0    0     2     3   25   50  3  1 96  0  0
```

---

## `vdir`

**Description:**  
Lists directory contents in a **long format**, similar to `ls -l`.

**Use Case:**  
Viewing detailed information about files including permissions, size, and modification dates.

### Example

```bash
vdir
```

**Output (Snippet)**

```
-rw-r--r-- 1 user user 245 Mar 10 21:01 notes.txt
-rwxr-xr-x 1 user user 512 Mar 10 20:58 script.sh
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
