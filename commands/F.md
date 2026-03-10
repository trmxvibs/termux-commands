# F Commands (Termux Edition)

Commands starting with the letter **F**.

---

## `false`

**Description:**  
A command that does nothing and simply returns a **non-zero exit status (failure)**.

**Use Case:**  
Testing error handling in shell scripts or intentionally forcing a command to fail inside logical conditions.

### Example

```bash
false
echo $?
```

**Output**

```
1
```

---

## `fg`

**Description:**  
Brings a **background or suspended job** back to the foreground.

**Use Case:**  
Continuing a paused program that was stopped using `Ctrl + Z`.

### Example

```bash
fg %1
```

**Output**

```
./long_running_script.sh
```

---

## `file`

**Description:**  
Determines the **type of a file** by inspecting its contents.

**Use Case:**  
Identifying unknown files, checking whether a file is a script, binary, or compressed archive.

### Example

```bash
file script.sh
```

**Output**

```
script.sh: Bourne-Again shell script, ASCII text executable
```

---

## `find`

**Description:**  
Searches for files and directories in a directory hierarchy based on name, size, type, or other conditions.

**Use Case:**  
Locating files when you don't remember their exact location.

### Example

```bash
find ~ -name "myscript.sh"
```

**Output**

```
/data/data/com.termux/files/home/projects/myscript.sh
```

---

## `free`

**Description:**  
Displays information about **memory usage**, including total, used, and free RAM.

**Use Case:**  
Checking how much RAM is available before running heavy programs.

### Example

```bash
free -h
```

**Output (Snippet)**

```
              total        used        free
Mem:          3.8G        1.2G        2.6G
Swap:         1.0G        0.0G        1.0G
```

---

## `fold`

**Description:**  
Wraps long lines in text files so that they fit within a specified width.

**Use Case:**  
Formatting long lines of text so they display properly in the terminal.

### Example

```bash
fold -w 20 long_text.txt
```

**Output**

```
This is a very long
line of text that
has been wrapped
into smaller parts
```

---

## `ftp`

**Description:**  
A command-line **File Transfer Protocol client** used to transfer files between a local machine and a remote server.

**Use Case:**  
Uploading or downloading files from FTP servers.

### Example

```bash
ftp ftp.example.com
```

**Output**

```
Connected to ftp.example.com
Name (ftp.example.com:user):
```

---

