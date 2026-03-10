# L Commands (Termux Edition)

Commands starting with the letter **L**.

---

## `ls`

**Description:**  
Lists the contents of a directory, including files and subdirectories.

**Use Case:**  
Viewing files in the current directory or inspecting folder contents.

### Example

```bash
ls
```

**Output**

```
backup.txt  myscript.sh  projects  storage
```

Example with details:

```bash
ls -la
```

**Output (Snippet)**

```
drwx------  5 user user 4096 Mar 10 21:10 .
drwx------ 10 user user 4096 Mar 10 20:55 ..
-rw-r--r--  1 user user  245 Mar 10 21:01 notes.txt
```

---

## `ln`

**Description:**  
Creates **links between files**. There are two types of links:  
- **Hard links**
- **Symbolic links (symlinks)**

**Use Case:**  
Creating shortcuts or references to files and directories.

### Example

Create a symbolic link:

```bash
ln -s original.txt shortcut.txt
```

**Output**

```
(A symbolic link named shortcut.txt is created.)
```

---

## `less`

**Description:**  
A pager program used to **view large files one screen at a time**.

**Use Case:**  
Reading large log files or configuration files without loading the entire file into memory.

### Example

```bash
less logfile.txt
```

**Output**

```
(The file opens in an interactive viewer.)
```

Useful keys inside `less`:

```
Space → next page
b     → previous page
q     → quit
```

---

## `locate`

**Description:**  
Searches for files using a **prebuilt database of file paths**, making it much faster than `find`.

**Use Case:**  
Quickly locating files anywhere in the system.

> Install if not available:

```bash
pkg install mlocate
```

### Example

```bash
locate myscript.sh
```

**Output**

```
/data/data/com.termux/files/home/scripts/myscript.sh
```

---

## `lsof`

**Description:**  
Stands for **"list open files"**. It shows which files are currently open by processes.

**Use Case:**  
Identifying which program is using a file, network port, or device.

### Example

```bash
lsof
```

**Output (Snippet)**

```
COMMAND  PID USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
bash    1234 user  cwd    DIR  253,0     4096 1234 /home/user
```

---

## `login`

**Description:**  
Starts a **new login session** for a user.

**Use Case:**  
Authenticating a user in multi-user systems.

### Example

```bash
login
```

**Output**

```
login: username
Password:
```

> Note: Rarely used in Termux due to its single-user environment.

---

## `logout`

**Description:**  
Ends the current login session.

**Use Case:**  
Exiting a user session in multi-user environments.

### Example

```bash
logout
```

**Output**

```
(Session terminated.)
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
