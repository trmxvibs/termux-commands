# O Commands (Termux Edition)

Commands starting with the letter **O**.

---

## `od`

**Description:**  
Short for **"octal dump"**. It displays the contents of a file in various formats such as **octal, hexadecimal, decimal, or ASCII**.

**Use Case:**  
Inspecting binary files, debugging corrupted files, or analyzing raw file data.

### Example

```bash
od file.bin
```

**Output (Snippet)**

```
0000000 21150 04716 00012 00000
0000020 00000 00000
```

Example with hexadecimal format:

```bash
od -x file.bin
```

---

## `openssl`

**Description:**  
A powerful toolkit used for **cryptography, encryption, SSL/TLS certificate management, and hashing**.

**Use Case:**  
Generating SSL certificates, encrypting files, creating hashes, or testing secure connections.

### Example

Generate SHA256 hash:

```bash
openssl dgst -sha256 file.txt
```

**Output**

```
SHA256(file.txt)= 3a7bd3e2360a3d29eea436fcfb7e44c
```

Example: Generate a private key

```bash
openssl genrsa -out private.key 2048
```

---

## `open`

**Description:**  
Opens files or URLs using the **default Android application** from within Termux.

**Use Case:**  
Opening a webpage in the browser or launching files stored on the device.

### Example

```bash
termux-open https://google.com
```

**Output**

```
(The default Android browser opens the website.)
```

Example opening a file:

```bash
termux-open image.jpg
```

---

## `objdump`

**Description:**  
Displays detailed information about **binary files and compiled programs**.

**Use Case:**  
Analyzing compiled executables, debugging binaries, or reverse engineering.

### Example

```bash
objdump -d program
```

**Output (Snippet)**

```
08048400 <main>:
 8048400: 55                    push   %ebp
 8048401: 89 e5                 mov    %esp,%ebp
```

---

## `openssl rand`

**Description:**  
Generates **cryptographically secure random numbers or strings**.

**Use Case:**  
Generating passwords, tokens, or cryptographic keys.

### Example

```bash
openssl rand -hex 16
```

**Output**

```
9f2a3c1d8e4b7a6c5d3e1f0a2b4c6d7e
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
