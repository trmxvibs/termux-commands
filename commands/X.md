# X Commands (Termux Edition)

Commands starting with the letter **X**.

---

## `xargs`

**Description:**  
Builds and executes command lines from **standard input**. It takes input (often from pipes) and passes it as arguments to another command.

**Use Case:**  
Processing multiple files or inputs efficiently, especially when combined with commands like `find`.

### Example

```bash
echo "file1.txt file2.txt" | xargs rm
```

**Output**

```
(file1.txt and file2.txt are removed.)
```

Example with `find`:

```bash
find . -name "*.log" | xargs rm
```

This deletes all `.log` files found in the directory.

---

## `xxd`

**Description:**  
Creates a **hexadecimal dump** of a file and can also convert a hex dump back into binary.

**Use Case:**  
Inspecting binary files, debugging corrupted files, or analyzing file structures.

### Example

```bash
xxd file.bin
```

**Output (Snippet)**

```
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR
```

Convert hex dump back to binary:

```bash
xxd -r hexfile.txt output.bin
```

---

## `xclip`

**Description:**  
A command-line utility used to **access the system clipboard** from the terminal.

**Use Case:**  
Copying command output to the clipboard or pasting clipboard content into files.

> Install if not available:

```bash
pkg install xclip
```

### Example

Copy text to clipboard:

```bash
echo "Hello Termux" | xclip -selection clipboard
```

Paste clipboard content:

```bash
xclip -selection clipboard -o
```

**Output**

```
Hello Termux
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
