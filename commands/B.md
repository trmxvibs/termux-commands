# B Commands

---

## `base64`

**Description:**  
Encodes and decodes data or text using Base64 encoding.

**Use Case:**  
Safely encoding text or binary data within shell scripts, or decoding hidden strings.

### Example

```bash
echo "Termux" | base64
```

**Output**

```
VGVybXV4Cg==
```

---

## `bash`

**Description:**  
The **Bourne Again Shell**. It is the default command-line shell used in Termux.  
It interprets and executes user commands and shell scripts.

**Use Case:**  
Executing `.sh` script files or starting a new shell session.  
It is useful for running a script that doesn't have execute permissions yet.

### Example

```bash
# Assuming you have a script named myscript.sh
bash myscript.sh
```

**Output (Example)**

```
Hello, Welcome to Termux Scripting!
```

*(Actual output depends on the script.)*

---

## `bc`

**Description:**  
An **arbitrary precision calculator language** used for advanced mathematical calculations in the terminal.

> **Note:** You may need to install it first.

```bash
pkg install bc
```

**Use Case:**  
Performing quick calculations, especially **floating-point (decimal) math**, which bash cannot handle natively.

### Example

```bash
# Calculate 10 divided by 3 with decimal points
echo "10 / 3" | bc -l
```

**Output**

```
3.33333333333333333333
```

---

## `bg`

**Description:**  
Resumes a suspended (paused) job and runs it in the **background**.  
In Termux, you can pause a running task by pressing **Ctrl + Z**.

**Use Case:**  
Freeing up your terminal while a long-running process continues running in the background.

### Example

```bash
bg %1
```

**Output**

```
[1]+ ./long_running_script.sh &
```

---

## `bind`

**Description:**  
Displays or modifies **keyboard layouts and keybindings** for the bash readline interface.

**Use Case:**  
Customizing terminal shortcuts or checking what a specific keyboard combination does.

### Example

```bash
# Search for the keybind that clears the screen
bind -P | grep "clear-screen"
```

**Output**

```
clear-screen can be found on "\C-l".
```

---

## `bzip2`

**Description:**  
A high-quality **file compression tool** that compresses files and replaces them with a `.bz2` version.

**Use Case:**  
Compressing large text files, logs, or scripts to save storage space on your Android device.

### Example

```bash
# Compress file.txt and show verbose output
bzip2 -v file.txt
```

**Output (Snippet)**

```
file.txt:  2.13:1,  3.76 bits/byte, 53.03% saved, 1204 in, 566 out.
```

---

