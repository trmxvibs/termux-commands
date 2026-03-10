# C Commands 

Commands starting with the letter **C**.

---

## `cat`

**Description:**  
Short for **"concatenate"**. It reads data from files and outputs their contents directly to the terminal screen.

**Use Case:**  
Quickly reading the contents of a small text file, configuration file, or script without opening a full text editor like `nano` or `vim`.

### Example

```bash
cat ~/.bash_history
```

**Output (Snippet)**

```
pkg update
pkg install python
ls -la
cd
```

---

## `cd`

**Description:**  
Stands for **"change directory"**. It is used to navigate between different folders within the Termux file system.

**Use Case:**  
Moving from your home directory to another location, such as accessing your Android phone's internal storage (after running `termux-setup-storage`).

### Example

```bash
# Move to the Android downloads folder
cd ~/storage/downloads
```

**Output**

```
(No text output if successful, but the terminal prompt changes to the new directory.)
```

---

## `chmod`

**Description:**  
Stands for **"change mode"**. It modifies the **read, write, and execute permissions** of a file or directory.

**Use Case:**  
Making a newly written bash or python script executable so it can be run directly from the terminal.

### Example

```bash
# Give execute permission to a script
chmod +x myscript.sh
```

**Output**

```
(Returns silently to the prompt if successful.)
```

---

## `chown`

**Description:**  
Stands for **"change owner"**. It changes the **user and/or group ownership** of a file or directory.

> **Note:** In Termux's single-user environment, this command is rarely needed unless fixing ownership issues.

**Use Case:**  
Correcting file ownership when files transferred from Android storage refuse to open or execute.

### Example

```bash
chown root:root myfile.txt
```

**Output**

```
(Returns silently if successful. Root ownership works only if the device is rooted and you are using tsu.)
```

---

## `clear`

**Description:**  
Clears the terminal screen of all previous commands and outputs.

**Use Case:**  
Cleaning the terminal workspace when the screen becomes cluttered with long command outputs.

### Example

```bash
clear
```

**Output**

```
(The screen is cleared, leaving only the terminal prompt.)
```

---

## `cp`

**Description:**  
Stands for **"copy"**. It copies files or entire directories from a source location to a destination location.

**Use Case:**  
Creating backups of configuration files or duplicating scripts.

### Example

```bash
# Copy a file and name the copy 'backup.txt'
cp config.txt backup.txt
```

**Output**

```
(Returns silently to the prompt if successful.)
```

---

## `curl`

**Description:**  
Short for **"Client URL"**. It is a powerful command-line tool used to transfer data to or from a server using protocols such as **HTTP, HTTPS, FTP**, and more.

**Use Case:**  
Downloading scripts directly from GitHub, making API requests, or testing website connectivity.

### Example

```bash
# Download a file and save it with its original name
curl -O https://raw.githubusercontent.com/termux/termux-packages/master/README.md
```

**Output (Snippet)**

```
% Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
Dload  Upload   Total   Spent    Left  Speed
100  4523  100  4523    0     0  12500      0 --:--:-- --:--:-- --:--:-- 12500
```

---

