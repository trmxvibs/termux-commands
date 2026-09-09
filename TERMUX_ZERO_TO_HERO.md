# 📱 Termux Zero to Hero — Complete Course

> Is file ko apne repo `trmxvibs/termux-commands` me root me daal dijiye (ya `COURSE.md` naam se). Ye ek complete beginner-to-advanced course hai — installation se lekar scripting, networking, programming languages, customization aur security tools tak, sab kuch step-by-step.

---

## 📚 Table of Contents

| # | Module | Kya seekhoge |
|---|--------|---------------|
| 0 | [Termux Kya Hai](#module-0--termux-kya-hai) | Basics samajhna |
| 1 | [Installation](#module-1--installation) | Sahi tarike se install karna |
| 2 | [First-Time Setup](#module-2--first-time-setup) | Storage, update, permissions |
| 3 | [Terminal Basics](#module-3--terminal-basics) | Navigation commands |
| 4 | [File Viewing & Editing](#module-4--file-viewing--editing) | cat, nano, vim |
| 5 | [Permissions & Ownership](#module-5--permissions--ownership) | chmod, chown |
| 6 | [Package Management](#module-6--package-management) | pkg, apt, dpkg |
| 7 | [Environment Variables & Aliases](#module-7--environment-variables--aliases) | export, alias, .bashrc |
| 8 | [Text Processing](#module-8--text-processing) | grep, awk, sed |
| 9 | [Archiving & Compression](#module-9--archiving--compression) | tar, zip, unzip |
| 10 | [Networking](#module-10--networking) | ping, curl, wget, ssh |
| 11 | [System Monitoring](#module-11--system-monitoring) | ps, htop, df |
| 12 | [Shell Scripting & Automation](#module-12--shell-scripting--automation) | Bash scripts, cron jobs |
| 13 | [Termux-API (Hardware)](#module-13--termux-api-hardware) | Camera, GPS, SMS, battery |
| 14 | [Git & GitHub](#module-14--git--github) | Version control |
| 15 | [Programming Languages Setup](#module-15--programming-languages-setup) | Python, Node, C, Java, PHP |
| 16 | [Local Servers](#module-16--local-servers) | HTTP server, Node/Express |
| 17 | [Termux Customization](#module-17--termux-customization) | zsh, themes, fonts, styling |
| 18 | [GUI / Desktop in Termux](#module-18--gui--desktop-in-termux) | XFCE + VNC |
| 19 | [Security & Networking Tools (Ethical Use)](#module-19--security--networking-tools-ethical-use) | nmap, sqlmap overview |
| 20 | [Troubleshooting](#module-20--troubleshooting) | Common errors fix |
| 21 | [Capstone Project](#module-21--capstone-project) | Sab kuch ek jagah |
| 22 | [Next Steps](#module-22--next-steps) | Aage kya seekhein |

---

## Module 0 — Termux Kya Hai

Termux ek **Android terminal emulator + Linux environment** hai jo bina root ke chalta hai. Isse aap:

- Linux commands run kar sakte ho
- Programming languages install kar sakte ho (Python, Node, C, etc.)
- Networking tools use kar sakte ho
- Automation scripts likh sakte ho
- Ek chhota development machine bana sakte ho apne phone ko

**Zaroori baat:** Termux Linux nahi hai, ye Linux jaisa environment deta hai Android ke upar (proot/chroot nahi, native packages `pkg` se milte hain).

---

## Module 1 — Installation

⚠️ **Google Play Store wala Termux purana ho chuka hai aur ab update nahi hota.** Hamesha ye do sources use karo:

### Option A: F-Droid (Recommended)

1. F-Droid app install karo: https://f-droid.org/
2. F-Droid me "Termux" search karo
3. Install karo

### Option B: GitHub Releases (Direct APK)

1. https://github.com/termux/termux-app/releases par jao
2. Latest release ka `.apk` download karo (apne phone ke architecture ke hisaab se — zyadatar `arm64-v8a`)
3. APK install karo (Unknown Sources allow karna padega)

### Zaroori Companion Apps (Optional but useful)

| App | Kaam |
|---|---|
| Termux:API | Hardware access (camera, GPS, SMS) |
| Termux:Styling | Themes & fonts |
| Termux:Widget | Home screen shortcuts |
| Termux:Boot | Boot par scripts chalana |

Sab F-Droid par milte hain — same source se lena zaroori hai warna signature mismatch error aayega.

---

## Module 2 — First-Time Setup

Termux open karte hi ye commands sabse pehle chalao:

```bash
pkg update && pkg upgrade -y
termux-setup-storage
```

- `pkg update && pkg upgrade` → sabhi packages latest version me update karta hai
- `termux-setup-storage` → phone storage access allow karta hai (`~/storage/` folder ban jaata hai)

Check karo storage access:

```bash
cd ~/storage/downloads
ls
```

Keyboard tips:
- Volume Down + C = Ctrl+C (process cancel)
- Volume Down + L = Pipe `|`
- Long press screen = Extra keys (Tab, Esc, arrows)

---

## Module 3 — Terminal Basics

| Command | Purpose |
|---|---|
| `pwd` | Current directory dikhata hai |
| `ls` | Files/folders list karta hai (`ls -la` = hidden files sahit detail) |
| `cd foldername` | Directory change karta hai (`cd ..` = ek level upar) |
| `mkdir name` | Naya folder banata hai |
| `touch file.txt` | Empty file banata hai |
| `rm file.txt` | File delete karta hai (`rm -r folder` = folder delete) |
| `cp source dest` | Copy karta hai |
| `mv source dest` | Move ya rename karta hai |
| `clear` | Screen clear karta hai |
| `history` | Pehle type kiye commands dikhata hai |

**Practice:**

```bash
mkdir my_scripts
cd my_scripts
touch hello.sh
ls -la
pwd
```

---

## Module 4 — File Viewing & Editing

| Command | Purpose |
|---|---|
| `cat file.txt` | Poora file content dikhata hai |
| `less file.txt` | Page-by-page view (q se exit) |
| `head file.txt` | Pehli 10 lines |
| `tail file.txt` | Aakhri 10 lines (`tail -f` = live logs) |
| `nano file.txt` | Beginner-friendly editor |
| `vim file.txt` | Advanced editor |

**nano cheatsheet:**
```
Ctrl + O → Save
Ctrl + X → Exit
Ctrl + K → Line cut
Ctrl + U → Line paste
```

**vim cheatsheet (basic):**
```
i        → Insert mode
Esc      → Command mode
:w       → Save
:q       → Quit
:wq      → Save & quit
```

---

## Module 5 — Permissions & Ownership

Linux me har file/folder ke 3 permission types hote hain: **Read (r), Write (w), Execute (x)** — Owner, Group, Others ke liye.

| Command | Purpose |
|---|---|
| `chmod +x script.sh` | Script ko executable banata hai |
| `chmod 755 file` | Numeric permission set karta hai |
| `whoami` | Current user dikhata hai |
| `id` | User/group info |
| `ls -l` | Permissions dikhata hai (`-rwxr-xr-x`) |

**Example:**
```bash
nano hello.sh
chmod +x hello.sh
./hello.sh
```

---

## Module 6 — Package Management

Termux `pkg` (apt ka wrapper) use karta hai.

| Command | Purpose |
|---|---|
| `pkg search name` | Package search karo |
| `pkg install name` | Install karo |
| `pkg uninstall name` | Remove karo |
| `pkg list-installed` | Installed packages list |
| `pkg upgrade` | Sabko update karo |
| `apt list --installed` | Detailed installed list |
| `dpkg -i file.deb` | Local `.deb` install karo |

**Example:**
```bash
pkg search python
pkg install python -y
python --version
```

---

## Module 7 — Environment Variables & Aliases

| Command | Purpose |
|---|---|
| `env` | Sabhi environment variables dikhao |
| `export VAR=value` | Naya variable banao |
| `echo $PATH` | PATH variable dekho |
| `alias ll='ls -la'` | Shortcut command banao |

Permanent banane ke liye `~/.bashrc` file me daalo:

```bash
nano ~/.bashrc
```
Add karo:
```bash
alias update='pkg update && pkg upgrade -y'
export EDITOR=nano
```
Save karke:
```bash
source ~/.bashrc
```

---

## Module 8 — Text Processing

| Command | Purpose |
|---|---|
| `grep "text" file` | Pattern search karo |
| `awk '{print $1}' file` | Columns extract karo |
| `sed 's/old/new/g' file` | Text replace karo |
| `sort file` | Lines sort karo |
| `uniq` | Duplicate lines hatao |
| `cut -d',' -f1 file` | Delimiter se column nikaalo |
| `wc -l file` | Lines count karo |

**Example:**
```bash
grep "ERROR" server_log.txt
cat file.csv | cut -d',' -f2
```

---

## Module 9 — Archiving & Compression

| Command | Purpose |
|---|---|
| `tar -cvf out.tar folder/` | Tar archive banao |
| `tar -xvf out.tar` | Extract karo |
| `tar -czvf out.tar.gz folder/` | Gzip compressed archive |
| `zip -r out.zip folder/` | Zip banao |
| `unzip file.zip` | Zip extract karo |

**Example:**
```bash
unzip project-master.zip
cd project-master
```

---

## Module 10 — Networking

| Command | Purpose |
|---|---|
| `ping google.com` | Connection test |
| `curl url` | Web/API data fetch karo |
| `wget url` | File download karo |
| `ip a` / `ifconfig` | IP address dikhao |
| `ssh user@host` | Remote login |
| `scp file user@host:/path` | Secure file transfer |
| `whois domain.com` | Domain info |

**Example:**
```bash
pkg install curl wget openssh
curl -I https://example.com
wget https://example.com/file.zip
```

---

## Module 11 — System Monitoring

| Command | Purpose |
|---|---|
| `ps aux` | Running processes |
| `htop` | Interactive process monitor |
| `df -h` | Disk usage |
| `du -sh folder/` | Folder size |
| `top` | Live resource usage |
| `termux-wake-lock` | Phone ko sleep hone se roko (long tasks ke liye) |
| `termux-wake-unlock` | Wake lock hatao |

**Example:**
```bash
pkg install htop
htop
```

---

## Module 12 — Shell Scripting & Automation

### Basic Bash Script

```bash
#!/bin/bash
echo "Termux Maintenance Start"

termux-wake-lock
pkg update -y
pkg upgrade -y
pkg clean
termux-wake-unlock

echo "System updated successfully!"
```

```bash
chmod +x update_all.sh
./update_all.sh
```

### Variables, Loops & Conditions

```bash
#!/bin/bash
name="Termux"

for i in 1 2 3; do
  echo "Hello $name, count: $i"
done

if [ -f "hello.sh" ]; then
  echo "File exists"
else
  echo "File not found"
fi
```

### Scheduling Tasks (No root needed)

```bash
pkg install termux-services cronie
sv-enable crond
crontab -e
```
Cron line example (har din 8 baje chalega):
```
0 8 * * * bash ~/update_all.sh
```

Boot par script chalane ke liye **Termux:Boot** app install karo aur script `~/.termux/boot/` folder me daalo.

---

## Module 13 — Termux-API (Hardware)

Pehle Termux:API app (F-Droid) + package install karo:

```bash
pkg install termux-api
```

| Command | Purpose |
|---|---|
| `termux-battery-status` | Battery info JSON |
| `termux-camera-photo photo.jpg` | Photo click karo |
| `termux-location` | GPS location |
| `termux-sms-list` | SMS messages padho |
| `termux-torch on/off` | Flashlight control |
| `termux-clipboard-get/set` | Clipboard access |
| `termux-vibrate` | Phone vibrate karo |
| `termux-notification` | Notification bhejo |

**Example:**
```bash
termux-battery-status
termux-torch on
```

---

## Module 14 — Git & GitHub

```bash
pkg install git
git config --global user.name "YourName"
git config --global user.email "you@example.com"
```

| Command | Purpose |
|---|---|
| `git clone url` | Repo clone karo |
| `git add .` | Changes stage karo |
| `git commit -m "msg"` | Commit karo |
| `git push` | GitHub par upload karo |
| `git pull` | Latest changes lao |
| `git status` | Status check karo |

**Example:**
```bash
git clone https://github.com/trmxvibs/termux-commands.git
cd termux-commands
nano README.md
git add .
git commit -m "update readme"
git push
```

---

## Module 15 — Programming Languages Setup

| Language | Install Command | Run Command |
|---|---|---|
| Python | `pkg install python` | `python file.py` |
| Node.js | `pkg install nodejs` | `node file.js` |
| C/C++ | `pkg install clang` | `clang file.c -o out && ./out` |
| Java | `pkg install openjdk-17` | `javac File.java && java File` |
| PHP | `pkg install php` | `php -S localhost:8000` |
| Ruby | `pkg install ruby` | `ruby file.rb` |
| Go | `pkg install golang` | `go run file.go` |
| Rust | `pkg install rust` | `cargo run` |

Python virtual environment (recommended practice):
```bash
pkg install python
pip install virtualenv
python -m venv myenv
source myenv/bin/activate
pip install requests
```

---

## Module 16 — Local Servers

**Python quick server:**
```bash
python -m http.server 8080
```
Browser me open karo: `http://localhost:8080`

**Node.js Express server:**
```bash
pkg install nodejs
mkdir myapp && cd myapp
npm init -y
npm install express
```
`index.js`:
```javascript
const express = require('express');
const app = express();
app.get('/', (req, res) => res.send('Hello from Termux!'));
app.listen(3000, () => console.log('Server running on 3000'));
```
```bash
node index.js
```

---

## Module 17 — Termux Customization

### Zsh + Oh My Zsh

```bash
pkg install zsh git curl
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
chsh -s zsh
```

### Fonts & Colors

Termux:Styling app install karo, phone me long-press karke color scheme aur font choose karo.

### Custom Prompt / Motd

`~/.termux/termux.properties` file edit karke extra-keys row customize kar sakte ho:
```bash
mkdir -p ~/.termux
nano ~/.termux/termux.properties
```
```
extra-keys = [['ESC','/','-','HOME','UP','END','PGUP'],['TAB','CTRL','ALT','LEFT','DOWN','RIGHT','PGDN']]
```
```bash
termux-reload-settings
```

---

## Module 18 — GUI / Desktop in Termux

Full Linux desktop (XFCE) chalana:

```bash
pkg install x11-repo
pkg install xfce4 tigervnc
vncserver
```

Phone me VNC Viewer app install karo aur `localhost:1` (ya jo port diya ho) connect karo.

Stop karne ke liye:
```bash
vncserver -kill :1
```

---

## Module 19 — Security & Networking Tools (Ethical Use)

⚠️ **Sirf apne khud ke network/device par ya likhit permission ke saath legal security research ke liye use karo.** Bina permission kisi aur ke system par use karna illegal hai.

| Tool | Purpose |
|---|---|
| `nmap` | Network scanning — kaunse devices/ports open hain |
| `tshark` | Network packet analyzer |
| `hydra` | Password auditing (apne systems par) |
| `sqlmap` | Apni khud ki web app me SQL injection testing |

**Example (apne router par):**
```bash
pkg install nmap
nmap -sV 192.168.1.1
```

Detailed step-by-step exploitation guides is course ka part nahi hain — ye sirf tool-overview hai taaki aapko pata ho ye tools kis category me aate hain aur inhe kab (legally) use kiya jaata hai.

---

## Module 20 — Troubleshooting

| Problem | Solution |
|---|---|
| `pkg` command not found | Termux reinstall karo F-Droid se |
| Storage access nahi mil raha | `termux-setup-storage` phir se chalao, Android permission allow karo |
| Package install fail ho raha | `pkg update && pkg upgrade -y` phir try karo |
| `Unable to locate package` | Repo mirror change karo: `termux-change-repo` |
| Termux crash ho raha | RAM kam ho sakti hai — heavy tasks (compiling) ke liye `termux-wake-lock` use karo |
| Python pip install fail | `pkg install clang python-dev` pehle install karo |

---

## Module 21 — Capstone Project

**Project: Auto-Backup Script**

Ek script banao jo:
1. `~/storage/downloads` ke files ko zip kare
2. Zip file ko ek backup folder me move kare
3. Termux notification bheje jab complete ho jaaye

```bash
#!/bin/bash
DATE=$(date +%Y-%m-%d)
mkdir -p ~/backups
zip -r ~/backups/backup_$DATE.zip ~/storage/downloads
termux-notification --title "Backup Complete" --content "Backup saved: backup_$DATE.zip"
```

Isko `cron` ke through daily automate karo — Module 12 dekho.

---

## Module 22 — Next Steps

- `man command` ya `command --help` se har command ki full detail padho
- Roz 3-5 naye commands practice karo
- Apna GitHub repo banao aur scripts push karte raho
- Termux community: Reddit r/termux, official Termux Wiki (https://wiki.termux.com)
- Is repo ke A-Z command list (`commands/A.md` se `Z.md`) ko reference ki tarah use karo

---

### 🎯 Contribution

Isko apne repo me `COURSE.md` ya `LEARNING_PATH.md` ke साथ merge/replace kar sakte hain. README.md ke "Repository Navigation" table me ek row add kar dena:

```markdown
| [Zero to Hero Course](https://github.com/trmxvibs/termux-commands/blob/main/TERMUX_ZERO_TO_HERO.md) | Complete beginner → advanced course |
```
