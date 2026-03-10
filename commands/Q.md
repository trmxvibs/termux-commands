# Q Commands (Termux Edition)

Commands starting with the letter **Q**.

---

## `quota`

**Description:**  
Displays the **disk usage and limits** for a user or group on a filesystem.

**Use Case:**  
Checking how much disk space a user is allowed to use and how much has already been used.

### Example

```bash
quota
```

**Output (Example)**

```
Disk quotas for user user (uid 1000):
Filesystem  blocks   quota   limit   grace   files   quota   limit   grace
/dev/sda1   102400   200000  250000           120     0       0
```

> Note: Disk quota systems are rarely used in Termux because Android devices usually operate as single-user environments.

---

## `quotacheck`

**Description:**  
Scans a filesystem to **check and repair disk quota information**.

**Use Case:**  
Ensuring that disk usage records match actual disk usage.

### Example

```bash
quotacheck -avug
```

**Output (Snippet)**

```
Checking quotas for filesystem /dev/sda1
```

---

## `quotaon`

**Description:**  
Enables **disk quota enforcement** on a filesystem.

**Use Case:**  
Activating quota limits so users cannot exceed their allocated disk space.

### Example

```bash
quotaon /dev/sda1
```

**Output**

```
Quota system enabled on /dev/sda1
```

---

## `quotaoff`

**Description:**  
Disables **disk quota enforcement** on a filesystem.

**Use Case:**  
Temporarily turning off quota restrictions.

### Example

```bash
quotaoff /dev/sda1
```

**Output**

```
Quota system disabled on /dev/sda1
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
