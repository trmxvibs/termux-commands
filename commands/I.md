# I Commands (Termux Edition)

Commands starting with the letter **I**.

---

## `id`

**Description:**  
Displays the **user identity information**, including user ID (UID), group ID (GID), and group memberships.

**Use Case:**  
Checking the current user’s permissions or verifying which user is running a command or script.

### Example

```bash
id
```

**Output**

```
uid=1000(u0_a123) gid=1000(u0_a123) groups=1000(u0_a123)
```

---

## `ifconfig`

**Description:**  
Displays or configures **network interfaces**.

**Use Case:**  
Checking your device's IP address, network status, or interface configuration.

> **Note:** Install if not available.

```bash
pkg install net-tools
```

### Example

```bash
ifconfig
```

**Output (Snippet)**

```
wlan0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>
inet 192.168.1.10  netmask 255.255.255.0
```

---

## `ip`

**Description:**  
A modern replacement for networking tools like `ifconfig`. It is used to **show or manipulate routing, network devices, and IP addresses**.

**Use Case:**  
Viewing network interfaces, IP addresses, and routing information.

### Example

```bash
ip addr
```

**Output (Snippet)**

```
2: wlan0: <BROADCAST,MULTICAST,UP,LOWER_UP>
inet 192.168.1.10/24 brd 192.168.1.255 scope global wlan0
```

---

## `install`

**Description:**  
Copies files and sets **ownership and permissions** at the same time.

**Use Case:**  
Installing scripts or binaries into system directories with proper permissions.

### Example

```bash
install myscript.sh ~/bin/myscript
```

**Output**

```
(Returns silently if successful.)
```

---

## `info`

**Description:**  
Displays **detailed documentation** for commands using the GNU Info system.

**Use Case:**  
Reading manuals and learning about advanced command options.

### Example

```bash
info ls
```

**Output**

```
GNU coreutils documentation for the 'ls' command opens in the info viewer.
```

---

## `ionice`

**Description:**  
Sets or displays the **I/O scheduling priority** of a process.

**Use Case:**  
Controlling disk usage priority for processes that read or write large amounts of data.

### Example

```bash
ionice -c 3 tar -czf backup.tar.gz folder/
```

**Output**

```
(Process runs with idle I/O priority.)
```

---

✔ This document is part of a **Termux Commands Reference Guide organized alphabetically**.
