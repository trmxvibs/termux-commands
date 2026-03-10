# M Commands (Termux Edition)

Commands starting with the letter **M**.

---

## `man`

**Description:**  
Displays the **manual page (documentation)** for a command.

**Use Case:**  
Learning how a command works, its options, and usage examples directly from the terminal.

> Install if not available:

```bash
pkg install man
```

### Example

```bash
man ls
```

**Output**

```
Manual page for the 'ls' command opens.
```

Inside the manual viewer:

```
Space → next page
b     → previous page
q     → quit
```

---

## `mkdir`

**Description:**  
Stands for **"make directory"**. It creates new directories.

**Use Case:**  
Organizing files by creating folders for projects, scripts, or downloads.

### Example

```bash
mkdir projects
```

**Output**

```
(A directory named 'projects' is created.)
```

Create nested directories:

```bash
mkdir -p projects/scripts/bash
```

---

## `mv`

**Description:**  
Moves or **renames files and directories**.

**Use Case:**  
Organizing files or renaming scripts.

### Example

Rename a file:

```bash
mv oldname.txt newname.txt
```

Move a file into a folder:

```bash
mv script.sh ~/projects/
```

**Output**

```
(Returns silently if successful.)
```

---

## `more`

**Description:**  
Displays file content **one screen at a time**.

**Use Case:**  
Viewing long files in the terminal without opening a full editor.

### Example

```bash
more logfile.txt
```

**Output**

```
(The file is displayed page by page.)
```

Navigation keys:

```
Space → next page
Enter → next line
q     → quit
```

---

## `mount`

**Description:**  
Attaches a filesystem to a directory so that it becomes accessible.

**Use Case:**  
Accessing external storage devices or mounted filesystems.

### Example

```bash
mount
```

**Output (Snippet)**

```
/dev/block/sda on /data type ext4 (rw,seclabel)
```

> Note: On Android/Termux many mount operations require root access.

---

## `make`

**Description:**  
A build automation tool that automatically compiles programs using instructions in a `Makefile`.

**Use Case:**  
Compiling software from source code.

### Example

```bash
make
```

**Output (Snippet)**

```
gcc -o program program.c
Compilation successful
```

---

## `md5sum`

**Description:**  
Calculates and verifies **MD5 checksums** for files.

**Use Case:**  
Verifying file integrity after downloads.

### Example

```bash
md5sum file.zip
```

**Output**

```
5d41402abc4b2a76b9719d911017c592  file.zip
```

Verify checksum from a list:

```bash
md5sum -c checksums.txt
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
