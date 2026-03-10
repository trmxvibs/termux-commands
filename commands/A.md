# A Commands 


---

## `alias`

**Description:**  
Creates a custom shortcut or nickname for a longer, more complex command string.

> **Note:** Aliases created in the terminal are temporary.  
> To make them permanent in **Termux**, add them to your `~/.bashrc` file.

**Use Case:**  
Saving time and reducing typos when executing repetitive or long commands on a mobile keyboard.

### Example

```bash
alias update="pkg update && pkg upgrade -y"
```

To view all active aliases:

```bash
alias
```

**Output**

```
alias update='pkg update && pkg upgrade -y'
```

---

## `am` (Android Activity Manager)

**Description:**  
A command-line tool specific to Android environments. In Termux, it interacts with the **Android Activity Manager** to start apps, broadcast intents, or open URLs directly from the terminal.

**Use Case:**  
Launching Android applications or opening web links without leaving the Termux terminal.

### Example

```bash
am start -a android.intent.action.VIEW -d "https://google.com"
```

**Output (Snippet)**

```
Starting: Intent { act=android.intent.action.VIEW dat=https://google.com }
```

---

## `apropos`

**Description:**  
Searches through **manual (man) page names and descriptions** for a specific keyword.

> **Note:** You may need to install the `man` package first.

```bash
pkg install man
```

**Use Case:**  
Finding a command when you know what it does but have forgotten its exact name.

### Example

```bash
apropos "make directories"
```

**Output**

```
mkdir (1) - make directories
```

---

## `apt`

**Description:**  
**Advanced Package Tool** used to install, update, and remove software.

> **Note:** Termux officially recommends using the `pkg` wrapper instead of `apt`.

**Use Case:**  
Installing new command-line tools or keeping the Termux environment up-to-date.

> **Important:** Do **not use `sudo` in Termux** because it runs in a single-user environment.

### Example

```bash
apt install python
```

**Output (Snippet)**

```
Reading package lists... Done
Building dependency tree... Done
The following NEW packages will be installed:
  python
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
```

---

## `arch`

**Description:**  
Prints the device's **hardware architecture**.

In Termux, this usually returns an **ARM-based architecture**, which is important when downloading compiled binaries.

**Use Case:**  
Checking whether your Android device is **32-bit or 64-bit** before downloading tools or binaries.

### Example

```bash
arch
```

**Output**

```
aarch64
```

> `aarch64` means **64-bit ARM**, which is standard for most modern Android phones.

---

## `awk`

**Description:**  
A powerful **text processing tool** used to scan files or command outputs line-by-line and split them into columns (fields).

**Use Case:**  
Filtering command outputs or extracting specific data without needing a full scripting language like Python.

### Example

```bash
echo "Termux is awesome" | awk '{print $1, $3}'
```

**Output**

```
Termux awesome
```

---

