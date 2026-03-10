# J Commands (Termux Edition)

Commands starting with the letter **J**.

---

## `jobs`

**Description:**  
Displays the list of **active jobs** (background or suspended processes) in the current shell session.

**Use Case:**  
Checking which programs are running in the background or paused.

### Example

```bash
jobs
```

**Output**

```
[1]+  Running    python server.py &
[2]-  Stopped    nano notes.txt
```

Example: resume job in foreground

```bash
fg %1
```

---

## `join`

**Description:**  
Combines lines of two files based on a **common field** (similar to a database join).

**Use Case:**  
Merging data from two files that share a common column.

### Example

File1:

```
1 Alice
2 Bob
```

File2:

```
1 Engineer
2 Designer
```

Command:

```bash
join file1.txt file2.txt
```

**Output**

```
1 Alice Engineer
2 Bob Designer
```

---

## `jq`

**Description:**  
A powerful **command-line JSON processor** used to parse, filter, and manipulate JSON data.

**Use Case:**  
Processing API responses, formatting JSON files, and extracting specific fields.

> Install if not available:

```bash
pkg install jq
```

### Example

```bash
echo '{"name":"Termux","type":"terminal"}' | jq '.name'
```

**Output**

```
"Termux"
```

Example extracting multiple fields:

```bash
jq '.name, .type' data.json
```

---

## `jps`

**Description:**  
Lists running **Java processes** along with their process IDs.

**Use Case:**  
Checking which Java applications are currently running.

> Requires Java installed.

### Example

```bash
jps
```

**Output**

```
1234 Main
5678 Jps
```

---

## `jar`

**Description:**  
A tool used to **create, extract, and manage Java Archive (.jar) files**.

**Use Case:**  
Packaging Java programs or extracting files from `.jar` archives.

### Example

Create jar:

```bash
jar cf app.jar *.class
```

Extract jar:

```bash
jar xf app.jar
```

**Output**

```
Files extracted from app.jar
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
