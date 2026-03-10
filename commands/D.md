# D Commands (Termux Edition)

Commands starting with the letter **D**.

---

## `date`

**Description:**  
Displays or sets the current system date and time.

**Use Case:**  
Checking the current time or adding timestamps to bash scripts and log files.

### Example

```bash
date
```

**Output**

```
Tue Mar 10 21:03:05 IST 2026
```

---

## `df`

**Description:**  
Stands for **"disk free"**. It reports the amount of available and used disk space on your device's file systems.

**Use Case:**  
Checking how much internal storage is available before downloading large packages or cloning large repositories.

> **Tip:** Use the `-h` flag for **human-readable format** (MB / GB).

### Example

```bash
df -h
```

**Output (Snippet)**

```
Filesystem       Size  Used Avail Use% Mounted on
/dev/block/sda   110G   85G   25G  78% /data
```

---

## `diff`

**Description:**  
Compares two files **line by line** and shows the differences between them.

**Use Case:**  
Checking what changes were made between two versions of a script.

### Example

```bash
# Compare two scripts
diff old_script.sh new_script.sh
```

**Output**

```
2c2
< echo "Hello World"
---
> echo "Hello Termux"
```

---

## `dir`

**Description:**  
Lists the contents of a directory.  
It behaves similarly to the `ls` command.

**Use Case:**  
Quickly viewing files and folders in the current directory.

### Example

```bash
dir
```

**Output**

```
backup.txt  downloads  myscript.sh  storage
```

---

## `dos2unix`

**Description:**  
Converts text files from **Windows line endings (`\r\n`)** to **Unix/Linux format (`\n`)**.

> **Note:** Install it first if not available.

```bash
pkg install dos2unix
```

**Use Case:**  
Fixing script errors when a script written on Windows is executed in Termux.

### Example

```bash
dos2unix script_from_windows.sh
```

**Output**

```
dos2unix: converting file script_from_windows.sh to Unix format...
```

---

## `dpkg`

**Description:**  
The **Debian package manager** used to install `.deb` packages manually.

While `apt` or `pkg` downloads packages from repositories, `dpkg` installs packages that are already downloaded locally.

**Use Case:**  
Installing custom or offline `.deb` packages.

### Example

```bash
dpkg -i custom_tool_v1.deb
```

**Output (Snippet)**

```
Selecting previously unselected package custom-tool.
(Reading database ... 15023 files and directories currently installed.)
Preparing to unpack custom_tool_v1.deb ...
Unpacking custom-tool (1.0) ...
Setting up custom-tool (1.0) ...
```

---

## `du`

**Description:**  
Stands for **"disk usage"**. It estimates the storage usage of files and directories.

**Use Case:**  
Finding which folder is consuming the most storage.

> **Tip:** Use `-sh` for a human-readable summary.

### Example

```bash
# Check the size of the downloads folder
du -sh ~/storage/downloads
```

**Output**

```
1.2G    /data/data/com.termux/files/home/storage/downloads
```

---

