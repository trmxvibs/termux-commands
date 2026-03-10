# U Commands (Termux Edition)

Commands starting with the letter **U**.

---

## `uname`

**Description:**  
Displays **system information** such as the operating system name, kernel version, and machine architecture.

**Use Case:**  
Checking system details before installing software or debugging compatibility issues.

### Example

```bash
uname
```

**Output**

```
Linux
```

More detailed system information:

```bash
uname -a
```

**Output (Snippet)**

```
Linux localhost 5.10.43-android #1 SMP PREEMPT Tue Mar 9 10:22:41 UTC 2026 aarch64 Android
```

---

## `uptime`

**Description:**  
Shows how long the system has been running along with the current load average.

**Use Case:**  
Monitoring system uptime and load statistics.

### Example

```bash
uptime
```

**Output**

```
21:32:10 up 5:14, 1 user, load average: 0.15, 0.10, 0.05
```

---

## `uniq`

**Description:**  
Filters out **duplicate adjacent lines** in a file or input stream.

**Use Case:**  
Cleaning duplicate entries in sorted data.

### Example

```bash
uniq names.txt
```

**Output**

```
Alice
Bob
Charlie
```

Often used with `sort`:

```bash
sort names.txt | uniq
```

---

## `unzip`

**Description:**  
Extracts files from **ZIP archives**.

**Use Case:**  
Opening downloaded `.zip` files containing scripts, tools, or datasets.

### Example

```bash
unzip archive.zip
```

**Output (Snippet)**

```
Archive: archive.zip
 extracting: file1.txt
 extracting: file2.txt
```

Extract to a specific folder:

```bash
unzip archive.zip -d folder/
```

---

## `useradd`

**Description:**  
Creates a **new user account** on the system.

**Use Case:**  
Managing users on multi-user Linux systems.

### Example

```bash
useradd newuser
```

**Output**

```
(User account created.)
```

> Note: In Termux this command is rarely used because Android runs in a single-user environment.

---

## `userdel`

**Description:**  
Deletes a **user account** from the system.

**Use Case:**  
Removing users who no longer need access to the system.

### Example

```bash
userdel newuser
```

**Output**

```
(User account removed.)
```

> Note: Typically used on multi-user Linux systems, not commonly needed in Termux.

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
