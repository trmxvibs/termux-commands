# Z Commands (Termux Edition)

Commands starting with the letter **Z**.

---

## `zcat`

**Description:**  
Displays the contents of **compressed `.gz` files** without extracting them.

**Use Case:**  
Quickly reading compressed log files or archives without manually decompressing them.

### Example

```bash
zcat logfile.gz
```

**Output (Snippet)**

```
[INFO] Server started
[INFO] Connection established
[ERROR] Timeout occurred
```

This shows the contents directly in the terminal.

---

## `zip`

**Description:**  
Compresses files and directories into a **`.zip` archive**.

**Use Case:**  
Packaging multiple files for sharing, downloading, or storage.

> Install if not available:

```bash
pkg install zip
```

### Example

Create a zip archive:

```bash
zip archive.zip file1.txt file2.txt
```

**Output (Snippet)**

```
adding: file1.txt (deflated 45%)
adding: file2.txt (deflated 30%)
```

Zip an entire folder:

```bash
zip -r project.zip project/
```

---

## `zgrep`

**Description:**  
Searches inside **compressed `.gz` files** using `grep` functionality.

**Use Case:**  
Finding specific text in compressed log files.

### Example

```bash
zgrep "error" logfile.gz
```

**Output**

```
[ERROR] Database connection failed
```

---

## `zless`

**Description:**  
Allows you to **view compressed files interactively** using the `less` pager.

**Use Case:**  
Browsing `.gz` files page by page without extracting them.

### Example

```bash
zless logfile.gz
```

**Output**

```
(The compressed file opens in the less viewer.)
```

Navigation inside viewer:

```
Space → next page
b     → previous page
q     → quit
```

---

## `zmore`

**Description:**  
Similar to `zless`, but uses the **`more` pager** to view compressed files.

**Use Case:**  
Reading compressed files page by page directly in the terminal.

### Example

```bash
zmore logfile.gz
```

**Output**

```
(The compressed file is displayed page by page.)
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
