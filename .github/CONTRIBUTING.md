# Contributing to Termux Command Encyclopedia

Thank you for your interest in contributing.

This project aims to build the **most comprehensive Termux command documentation on GitHub**. Contributions from beginners and experienced users are both welcome.

---

# Ways to Contribute

You can help this project in many ways:

• Add new command documentation  
• Improve command explanations  
• Add examples or use cases  
• Fix spelling or grammar mistakes  
• Improve formatting  
• Add networking or security command guides  

---

# Project Structure

```
termux-command-encyclopedia
│
├── README.md
├── COMMAND_MASTER_LIST.md
├── COMMAND_INDEX.md
├── CHEATSHEET.md
├── LEARNING_PATH.md
├── NETWORKING.md
├── TERMUX_API.md
├── HACKING_TOOLS.md
├── LINUX_COMMAND_MINDMAP.md
│
├── commands
│   ├── A.md
│   ├── B.md
│   ├── C.md
│   └── ...
```
---

Commands are organized alphabetically.

Example:

```
commands/G.md
```

contains commands like:

```
git
grep
groups
```

---

# Adding a New Command

1 Fork the repository.

2 Clone your fork.

```
git clone https://github.com/trmxvibs/termux-commands
```

3 Navigate to repository.

```
cd termux-commands
```

4 Create a new branch.

```
git checkout -b add-command
```

5 Edit the correct command file.

Example:

```
commands/C.md
```

Add command documentation using this format:

```
## command_name

Description

Explain what the command does.

Syntax

```bash
command [options]
```

Example

```bash
example command
```

Use Case

Explain real world use.
```

6 Commit changes.

```
git add .
git commit -m "Added documentation for command_name"
```

7 Push your branch.

```
git push origin add-command
```

8 Open a Pull Request.

---

# Documentation Style Guide

Please follow these rules:

• Use **Markdown headings** properly  
• Provide **clear command examples**  
• Avoid unnecessary complexity  
• Keep explanations beginner friendly  

Example format:

```
## grep

Description

Search text patterns in files.

Example

```bash
grep "error" log.txt
```

Use Case
```
Finding error logs inside system files.
```

---

# Commit Message Guidelines

Good commit message examples:

```
Added documentation for grep command
Improved examples in curl documentation
Fixed typo in networking section
```

Avoid messages like:

```
update
changes
fix
```

---

# Pull Request Checklist

Before submitting your PR:

- [ ] Command explanation added
- [ ] Example included
- [ ] Markdown formatting correct
- [ ] File placed in correct alphabetical file

---

# Code of Conduct

Please follow these guidelines:

• Be respectful  
• Help beginners learn  
• Avoid offensive language  
• Focus on improving documentation  

---

# Reporting Issues

If you find errors in the documentation:

1 Go to the **Issues** tab
2 Click **New Issue**
3 Describe the problem clearly

Example:

```sh
Command: grep
Problem: Example command is incorrect
Suggested Fix: Replace example with grep "text" file.txt
```
---

# Good First Contributions

Beginner friendly tasks include:

• Add examples to commands  
• Fix formatting issues  
• Improve descriptions  
• Add missing commands  


# Thank You

Your contributions help build a better learning resource for the entire Termux community.
