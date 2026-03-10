# G Commands (Termux Edition)

Commands starting with the letter **G**.

---

## `getconf`

**Description:**  
Displays configuration values for the current system, such as limits, POSIX settings, and system variables.

**Use Case:**  
Checking system configuration values used by programs and scripts.

### Example

```bash
getconf PAGE_SIZE
```

**Output**

```
4096
```

---

## `git`

**Description:**  
A **distributed version control system** used to track changes in source code and collaborate with other developers.

**Use Case:**  
Cloning repositories, managing versions of scripts, and contributing to GitHub projects.

### Example

```bash
git clone https://github.com/termux/termux-packages.git
```

**Output (Snippet)**

```
Cloning into 'termux-packages'...
remote: Enumerating objects...
Receiving objects: 100% (xxxxx/xxxxx)
```

---

## `grep`

**Description:**  
Searches text for **patterns or keywords** within files.

**Use Case:**  
Finding specific lines inside logs, configuration files, or command outputs.

### Example

```bash
grep "error" logfile.txt
```

**Output**

```
[ERROR] connection failed
```

Example with pipe:

```bash
ps aux | grep python
```

---

## `groups`

**Description:**  
Displays the groups that the current user belongs to.

**Use Case:**  
Checking group membership, especially when troubleshooting permission issues.

### Example

```bash
groups
```

**Output**

```
u0_a123 inet everybody
```

---

## `gzip`

**Description:**  
A file compression utility that reduces file size using the **gzip compression algorithm**.

**Use Case:**  
Compressing large files to save storage or preparing files for transfer.

### Example

```bash
gzip file.txt
```

**Output**

```
file.txt.gz created
```

---

## `gunzip`

**Description:**  
Decompresses files that were compressed using `gzip`.

**Use Case:**  
Extracting `.gz` compressed files.

### Example

```bash
gunzip file.txt.gz
```

**Output**

```
file.txt restored
```

---

## `gpg`

**Description:**  
GNU Privacy Guard — a tool for **encryption, decryption, and signing data**.

**Use Case:**  
Securing files, verifying software downloads, and encrypting sensitive data.

### Example

```bash
gpg -c secret.txt
```

**Output**

```
Enter passphrase:
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
