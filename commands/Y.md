# Y Commands (Termux Edition)

Commands starting with the letter **Y**.

---

## `yes`

**Description:**  
Continuously outputs a string (by default the letter **"y"**) until the process is stopped.

**Use Case:**  
Automatically answering **yes** to prompts in scripts or commands that require confirmation.

### Example

```bash
yes
```

**Output (Snippet)**

```
y
y
y
y
y
```

Stop the command with:

```
Ctrl + C
```

Example with custom text:

```bash
yes Termux
```

**Output**

```
Termux
Termux
Termux
```

---

## `yes | command`

**Description:**  
Used to **automatically confirm prompts** for commands that ask for user confirmation.

**Use Case:**  
Automating installations or commands that repeatedly ask for confirmation.

### Example

```bash
yes | pkg upgrade
```

**Output (Snippet)**

```
Do you want to continue? [Y/n]
y
```

The `yes` command automatically sends `y` as input.

---

## `yarn`

**Description:**  
A **JavaScript package manager** used to manage dependencies in Node.js projects.

**Use Case:**  
Installing and managing libraries in JavaScript applications.

> Install if not available:

```bash
pkg install yarn
```

### Example

Install project dependencies:

```bash
yarn install
```

Add a package:

```bash
yarn add express
```

**Output (Snippet)**

```
success Saved lockfile.
success Installed packages.
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
