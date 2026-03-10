# R Commands (Termux Edition)

Commands starting with the letter **R**.

---

## `rm`

**Description:**  
Stands for **"remove"**. It deletes files or directories.

**Use Case:**  
Cleaning unnecessary files, removing old scripts, or clearing temporary data.

### Example

```bash
rm file.txt
```

**Output**

```
(File is deleted silently if successful.)
```

Delete directory recursively:

```bash
rm -r foldername
```

Force delete:

```bash
rm -rf foldername
```

⚠ **Warning:** `rm -rf` permanently deletes files and directories.

---

## `rmdir`

**Description:**  
Removes **empty directories**.

**Use Case:**  
Deleting folders that no longer contain files.

### Example

```bash
rmdir oldfolder
```

**Output**

```
(The empty directory is removed.)
```

If the directory contains files, the command will fail.

---

## `rsync`

**Description:**  
A powerful **file synchronization and transfer tool**.

**Use Case:**  
Copying large directories, creating backups, or syncing files between locations.

### Example

```bash
rsync -av source_folder/ backup_folder/
```

**Output (Snippet)**

```
sending incremental file list
file1.txt
file2.txt

sent 245 bytes  received 35 bytes
```

Common flags:

```
-a → archive mode
-v → verbose output
```

---

## `read`

**Description:**  
Reads user input from the terminal and stores it in a variable.

**Use Case:**  
Creating interactive shell scripts that require user input.

### Example

```bash
read name
echo "Hello $name"
```

**Output**

```
Lokesh
Hello Lokesh
```

---

## `reboot`

**Description:**  
Restarts the system.

**Use Case:**  
Rebooting the device after system updates or configuration changes.

### Example

```bash
reboot
```

**Output**

```
(The system begins the reboot process.)
```

> Note: On Android/Termux this command usually requires **root access**.

---

## `rename`

**Description:**  
Renames multiple files using patterns.

**Use Case:**  
Batch renaming files quickly.

### Example

```bash
rename 's/.txt/.log/' *.txt
```

**Output**

```
file1.txt → file1.log
file2.txt → file2.log
```

---

## `rev`

**Description:**  
Reverses the characters of each line in a file.

**Use Case:**  
Manipulating or analyzing text in reverse order.

### Example

```bash
echo "Termux" | rev
```

**Output**

```
xumreT
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
