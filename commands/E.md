# E Commands (Termux Edition)

Commands starting with the letter **E**.

---

## `echo`

**Description:**  
Prints text or variables to the terminal.

**Use Case:**  
Displaying messages in scripts, debugging shell scripts, or writing text into files.

### Example

```bash
echo "Hello Termux"
```

**Output**

```
Hello Termux
```

Example (write text into a file):

```bash
echo "Termux is powerful" > message.txt
```

---

## `env`

**Description:**  
Displays all environment variables currently set in the shell session.

**Use Case:**  
Checking variables such as `PATH`, `HOME`, or variables used by programs and scripts.

### Example

```bash
env
```

**Output (Snippet)**

```
HOME=/data/data/com.termux/files/home
PATH=/data/data/com.termux/files/usr/bin
LANG=en_US.UTF-8
```

---

## `exit`

**Description:**  
Exits the current shell session.

**Use Case:**  
Closing a Termux session or exiting from a subshell or script.

### Example

```bash
exit
```

**Output**

```
(The terminal session closes.)
```

---

## `expr`

**Description:**  
A command-line tool used to evaluate expressions such as arithmetic operations and string comparisons.

**Use Case:**  
Performing simple calculations or comparisons inside shell scripts.

### Example

```bash
expr 10 + 5
```

**Output**

```
15
```

Example (string length):

```bash
expr length "Termux"
```

Output

```
6
```

---

## `expand`

**Description:**  
Converts tab characters in a file into spaces.

**Use Case:**  
Cleaning formatting in text files or preparing code files where spaces are required instead of tabs.

### Example

```bash
expand file.txt
```

**Output**

```
(Tabs in the file are replaced with spaces.)
```

---

## `export`

**Description:**  
Sets environment variables that are available to child processes.

**Use Case:**  
Defining variables used by scripts or programs.

### Example

```bash
export EDITOR=nano
```

Check the variable:

```bash
echo $EDITOR
```

**Output**

```
nano
```

---

