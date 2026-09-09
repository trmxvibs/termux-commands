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
| 21 | [Advanced Bash Scripting](#module-21--advanced-bash-scripting) | Functions, arrays, string ops |
| 22 | [Linux Distros Inside Termux](#module-22--linux-distros-inside-termux-proot-distro) | proot-distro (Ubuntu/Kali) |
| 23 | [Advanced Networking](#module-23--advanced-networking) | SSH keys, tunneling, VPN |
| 24 | [Automation with Tasker/Widgets](#module-24--automation-with-termuxtasker--widgets) | Auto-run scripts |
| 25 | [Building & Publishing a CLI Tool](#module-25--building--publishing-your-own-cli-tool) | Python packaging, PyPI |
| 26 | [Service Management](#module-26--service-management-systemd-style-with-termux-services) | termux-services |
| 27 | [Machine Learning Basics](#module-27--machine-learning-basics-on-termux) | scikit-learn on device |
| 28 | [Full Stack Mini Project](#module-28--full-stack-mini-project-lamp-style) | PHP + SQLite server |
| 29 | [Interview/Troubleshooting Practice](#module-29--interview--real-world-troubleshooting-practice) | Real scenarios |
| 30 | [Working with APIs](#module-30--working-with-apis-curl--jq) | curl + jq, JSON parsing |
| 31 | [Real-World Mini Projects](#module-31--real-world-mini-projects) | Telegram bot, weather notifier, scraper, file organizer |
| 32 | [Termux + Docker/Containers](#module-32--termux--docker--containers) | proot-distro, remote Docker via SSH |
| 33 | [Voice & AI Tools](#module-33--voice--ai-tools-on-termux) | Speech-to-text, TTS, local LLM |
| 34 | [Android App Dev from Termux](#module-34--android-app-development-from-termux-build-an-apk) | Buildozer, Gradle, APK signing |
| 35 | [Capstone Project](#module-35--capstone-project) | Sab kuch ek jagah |
| 36 | [Next Steps](#module-36--next-steps) | Aage kya seekhein |
| 📎 | [**Appendix — Complete Reference**](#-appendix--complete-reference-sab-kuch-ek-jagah) | Directory structure, sab shortcuts, glossary, FAQ, error fixes, package list, backup/restore, aliases, 1-page cheat sheet |

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

## Module 21 — Advanced Bash Scripting

**Goal:** Bash ko sirf commands chalane ke liye nahi, balki real programming ke liye use karna seekho.

### Functions

```bash
#!/bin/bash
greet() {
  local name=$1
  echo "Hello, $name!"
}
greet "Termux User"
```

### Arrays

```bash
fruits=("apple" "banana" "mango")
echo "${fruits[0]}"        # apple
echo "${fruits[@]}"        # sabhi elements
echo "${#fruits[@]}"       # array length
```

### String Manipulation

```bash
str="Termux_Course"
echo "${str,,}"            # lowercase
echo "${str^^}"            # UPPERCASE
echo "${str/Course/Guide}" # replace
echo "${str:0:6}"          # substring
```

### Command Substitution & Exit Codes

```bash
today=$(date +%Y-%m-%d)
echo "Today is $today"

ping -c1 google.com > /dev/null 2>&1
if [ $? -eq 0 ]; then
  echo "Internet is working"
else
  echo "No internet"
fi
```

### Reading User Input & Argument Parsing

```bash
#!/bin/bash
read -p "Enter your name: " name
echo "Welcome $name"

# Script arguments: ./script.sh arg1 arg2
echo "First arg: $1"
echo "All args: $@"
echo "Total args: $#"
```

---

## Module 22 — Linux Distros Inside Termux (proot-distro)

Agar aapko poora Ubuntu/Debian/Kali/Alpine environment chahiye Termux ke andar (chroot jaisa, bina root ke):

```bash
pkg install proot-distro
proot-distro list
proot-distro install ubuntu
proot-distro login ubuntu
```

Login hone ke baad aap us distro ke andar `apt`, `sudo`, full package repos use kar sakte ho — jaise real Ubuntu machine.

Exit karne ke liye: `exit`
Distro remove karne ke liye: `proot-distro remove ubuntu`

**Use case:** Jab kisi tool ko sirf Debian/Ubuntu par test karna ho, ya jab Termux ke `pkg` repo me koi package na mile.

---

## Module 23 — Advanced Networking

### SSH Key-Based Login (password-less)

```bash
pkg install openssh
ssh-keygen -t ed25519
ssh-copy-id user@remote-host
ssh user@remote-host   # ab password nahi maangega
```

### Port Forwarding / SSH Tunneling

```bash
# Local port 8080 ko remote server ke port 80 se forward karo
ssh -L 8080:localhost:80 user@remote-host
```

### Reverse Shell Concept (educational, apne systems par hi test karo)

Reverse tunneling samajhna important hai networking ke liye, lekin isko sirf **apne khud ke test lab/servers** par try karo.

### Simple VPN awareness

Termux khud VPN server nahi chalata, but `wireguard-tools` package se WireGuard client config manage kar sakte ho:

```bash
pkg install wireguard-tools
```

---

## Module 24 — Automation with Termux:Tasker & Widgets

- **Termux:Widget** (F-Droid se install karo) → `~/.shortcuts/` folder me script daalo, home screen se ek-tap run hoga
- **Termux:Tasker** → Tasker app ke saath integrate karke triggers (jaise "jab charging start ho") par scripts chala sakte ho
- **Termux:Boot** → phone restart hone par scripts auto-run karne ke liye

```bash
mkdir -p ~/.shortcuts
nano ~/.shortcuts/backup.sh
chmod +x ~/.shortcuts/backup.sh
```

---

## Module 25 — Building & Publishing Your Own CLI Tool

**Goal:** Ek chhota Python CLI tool banao aur usse PyPI par publish karo (jaisa `pkgwrap` type tools hote hain).

```bash
pkg install python
pip install build twine
mkdir mytool && cd mytool
```

Basic structure:
```
mytool/
├── mytool/
│   └── __init__.py
├── pyproject.toml
└── README.md
```

Build & test locally:
```bash
python -m build
pip install dist/mytool-0.1.0-py3-none-any.whl
mytool --help
```

Publish (account chahiye pypi.org par):
```bash
twine upload dist/*
```

---

## Module 26 — Service Management (systemd-style with termux-services)

Termux me traditional `systemd` nahi hota, lekin `termux-services` isi jaisa kaam deta hai:

```bash
pkg install termux-services
sv-enable sshd
sv up sshd
sv down sshd
sv status sshd
```

Isse aap apne background services (SSH server, cron, custom daemons) ko manage kar sakte ho jaise ek real Linux server par.

---

## Module 27 — Machine Learning Basics on Termux

```bash
pkg install python
pip install numpy pandas scikit-learn
```

Chhota example:
```python
from sklearn.linear_model import LinearRegression
import numpy as np

X = np.array([[1], [2], [3], [4]])
y = np.array([2, 4, 6, 8])

model = LinearRegression().fit(X, y)
print(model.predict([[5]]))   # Output: ~10
```

TensorFlow Lite jaise heavy frameworks phone ki RAM/CPU ke hisaab se limited chalte hain — chhote models/experiments ke liye theek hai, production training ke liye nahi.

---

## Module 28 — Full Stack Mini Project (LAMP-style)

Ek complete backend stack Termux me chalao:

```bash
pkg install php sqlite mariadb
mkdir mywebapp && cd mywebapp
echo "<?php echo 'Hello from Termux Server'; ?>" > index.php
php -S 0.0.0.0:8080
```

Phone ke browser me open karo: `http://localhost:8080`

Database ke saath:
```bash
sqlite3 data.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
sqlite3 data.db "INSERT INTO users (name) VALUES ('Test User');"
sqlite3 data.db "SELECT * FROM users;"
```

---

## Module 29 — Interview / Real-World Troubleshooting Practice

Ye scenarios khud solve karke practice karo (ye asli developer/sysadmin interviews me poochhe jaate hain):

| Scenario | Command/Concept expected |
|---|---|
| Disk full ho gayi hai, kaunsa folder bada hai pata karo | `du -sh */ \| sort -rh` |
| Ek process port 8080 use kar raha hai, use band karo | `lsof -i :8080` then `kill -9 PID` |
| File me kisi specific word ka count nikaalo | `grep -c "word" file.txt` |
| Do files ka difference dekho | `diff file1 file2` |
| Background me chal rahe process ko dekhkar band karo | `ps aux \| grep name` then `kill PID` |
| Ek script har 5 minute me chale | Cron: `*/5 * * * * bash script.sh` |

---

## Module 30 — Working with APIs (curl + jq)

Real-world scripts aksar kisi API se data leke kaam karte hain. Yahan seekhoge kaise.

```bash
pkg install curl jq
```

**Example: Weather data ek API se fetch karo**
```bash
curl -s "https://wttr.in/Jodhpur?format=3"
```

**Example: JSON response ko parse karo**
```bash
curl -s "https://api.github.com/users/torvalds" | jq '.name, .public_repos, .followers'
```

`jq` cheatsheet:
| Syntax | Kaam |
|---|---|
| `jq '.'` | Pura JSON pretty-print karo |
| `jq '.key'` | Ek field nikaalo |
| `jq '.[0]'` | Array ka pehla element |
| `jq '.[] .name'` | Har object me se ek field nikaalo |

---

## Module 31 — Real-World Mini Projects

Ab tak seekhi cheezon ko combine karke chhote real tools banate hain:

### Project 1: Telegram Notification Bot (bina coding heavy)

```bash
pkg install curl
BOT_TOKEN="your_bot_token"
CHAT_ID="your_chat_id"

curl -s -X POST "https://api.telegram.org/bot$BOT_TOKEN/sendMessage" \
  -d chat_id="$CHAT_ID" \
  -d text="Termux se message aa raha hai!"
```
(BotFather se apna bot token lo, `@userinfobot` se apna chat_id lo)

### Project 2: Daily Weather Notifier (cron + termux-api)

```bash
#!/bin/bash
weather=$(curl -s "https://wttr.in/Jodhpur?format=3")
termux-notification --title "Aaj ka Mausam" --content "$weather"
```
Isko cron me daily 7 baje chalane ke liye:
```
0 7 * * * bash ~/weather_notify.sh
```

### Project 3: Simple Web Scraper (Python)

```bash
pkg install python
pip install requests beautifulsoup4
```
```python
import requests
from bs4 import BeautifulSoup

r = requests.get("https://news.ycombinator.com")
soup = BeautifulSoup(r.text, "html.parser")
titles = soup.select(".titleline a")

for t in titles[:10]:
    print(t.text)
```

### Project 4: File Organizer Script

```bash
#!/bin/bash
cd ~/storage/downloads
mkdir -p Images PDFs Others

for f in *; do
  case "$f" in
    *.jpg|*.png|*.jpeg) mv "$f" Images/ ;;
    *.pdf) mv "$f" PDFs/ ;;
    *) [ -f "$f" ] && mv "$f" Others/ ;;
  esac
done
echo "Downloads organized!"
```

---

## Module 32 — Termux + Docker / Containers

**Sach baat:** Stock (non-rooted) Android par **real Docker daemon nahi chalta** — kyunki Docker ko Linux kernel ke `cgroups` aur `namespaces` chahiye jo bina root ke Android kernel expose nahi karta. Lekin container-jaisa isolation paane ke 3 practical tareeke hain:

### Option A: proot-distro (already covered Module 22) — sabse aasan
```bash
pkg install proot-distro
proot-distro install ubuntu
proot-distro login ubuntu
```
Ye "container jaisa" isolated filesystem deta hai (namespaces ke bina, proot ke through) — development/testing ke liye kaafi hai.

### Option B: Remote Docker via SSH (asli Docker chahiye to)
Apne PC/VPS par Docker chalao, Termux se sirf control karo:
```bash
pkg install openssh
ssh user@your-server
# server par docker commands chalao
docker ps
docker run -it ubuntu bash
```
Ya Docker context use karke local Termux se remote daemon control karo:
```bash
docker context create remote --docker "host=ssh://user@your-server"
docker context use remote
docker ps
```

### Option C: Rooted device (advanced, risky)
Agar phone rooted hai aur custom kernel support karta hai, tab hi native Docker/Podman chalne ke chances hain — ye course ka scope nahi hai kyunki rooting risk bharra kaam hai.

**Practical suggestion:** Learning/dev ke liye Option A (proot-distro) use karo; production containers ke liye Option B (remote server) sabse reliable hai.

---

## Module 33 — Voice & AI Tools on Termux

### Speech-to-Text & Text-to-Speech (Termux:API)

```bash
pkg install termux-api
```

```bash
# Bolo aur text me convert ho jaayega
termux-speech-to-text

# Text ko bulwao
termux-tts-speak "Namaste, main Termux hoon"
```

### Chhota Voice-Command Script

```bash
#!/bin/bash
text=$(termux-speech-to-text)
echo "Aapne kaha: $text"

if [[ "$text" == *"time"* ]]; then
  termux-tts-speak "Abhi time hai $(date +%H:%M)"
elif [[ "$text" == *"battery"* ]]; then
  level=$(termux-battery-status | jq '.percentage')
  termux-tts-speak "Battery $level percent hai"
else
  termux-tts-speak "Maaf kijiye, samajh nahi aaya"
fi
```

### Local LLM Chalana (Offline AI, chhote models)

Bade AI models phone par chalna mushkil hai, lekin `llama.cpp` jaisa lightweight engine chhote **quantized (GGUF)** models chala sakta hai:

```bash
pkg install git cmake clang
git clone https://github.com/ggerganov/llama.cpp
cd llama.cpp
cmake -B build
cmake --build build --config Release
```
Fir ek chhota GGUF model (jaise 1B-3B parameter wala) download karke:
```bash
./build/bin/llama-cli -m model.gguf -p "Termux ke baare me batao"
```
⚠️ RAM/storage ki limit hoti hai — sirf **chhote (1B-3B) quantized models** hi realistically phone par chalte hain, bade models (7B+) slow ya crash ho sakte hain low-RAM devices par.

### Cloud AI API Use Karna (jab internet ho)

```bash
pkg install python
pip install requests
```
```python
import requests
response = requests.post(
    "https://api.anthropic.com/v1/messages",
    headers={"x-api-key": "YOUR_KEY", "anthropic-version": "2023-06-01"},
    json={"model": "claude-sonnet-4-6", "max_tokens": 200,
          "messages": [{"role": "user", "content": "Hello from Termux!"}]}
)
print(response.json())
```

---

## Module 34 — Android App Development from Termux (Build an APK)

⚠️ **Realistic expectation set karna zaroori hai:** Termux full **Android Studio** replace nahi karta — RAM/storage limits ki wajah se — lekin **chhote/simple APKs** command-line se banana possible hai.

### Method A: Python apps → APK via Buildozer (proot-distro ke andar, recommended)

```bash
proot-distro install ubuntu
proot-distro login ubuntu
apt update && apt install -y python3-pip git zip openjdk-17-jdk
pip install buildozer cython
```
Ek Kivy Python app folder me:
```bash
buildozer init
buildozer -v android debug
```
Output APK `bin/` folder me milega. ⚠️ Ye process **bahut storage (5-10GB+) aur time** leta hai — powerful phone (6GB+ RAM) recommended hai.

### Method B: Native tools directly Termux me (chhote/manual APKs ke liye)

```bash
pkg install aapt apksigner dx ecj openjdk-17
```
Ye tools manually `.apk` package karne, sign karne ke liye use hote hain — ye advanced/educational route hai, real projects ke liye Method A behtar hai.

### Method C: Gradle-based Android project build karna

Agar aapke paas already ek Android project (Java/Kotlin, Gradle) hai:
```bash
pkg install openjdk-17
proot-distro login ubuntu   # Android SDK ke saath better compatibility ke liye
cd my-android-project
./gradlew assembleDebug
```
Output: `app/build/outputs/apk/debug/app-debug.apk`

**Sacchai:** Complex/large Android apps build karna phone par slow aur resource-heavy hota hai. Chhote personal projects/learning ke liye theek hai, professional development ke liye laptop/PC hi best rahega.

---

## Module 35 — Capstone Project

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

## Module 36 — Next Steps

- `man command` ya `command --help` se har command ki full detail padho
- Roz 3-5 naye commands practice karo
- Apna GitHub repo banao aur scripts push karte raho
- Termux community: Reddit r/termux, official Termux Wiki (https://wiki.termux.com)
- Is repo ke A-Z command list (`commands/A.md` se `Z.md`) ko reference ki tarah use karo

---

---
---

# 📎 APPENDIX — Complete Reference (Sab Kuch Ek Jagah)

> Ye section is liye hai taaki course padhne ke baad aapko **kahin aur na jaana pade**. Har chhoti-badi detail yahan hai.

## 📑 Appendix Table of Contents

- [A1. Termux Directory Structure Explained](#a1-termux-directory-structure-explained)
- [A2. Complete Keyboard & Editor Shortcuts](#a2-complete-keyboard--editor-shortcuts)
- [A3. Glossary — Har Term Ka Matlab](#a3-glossary--har-term-ka-matlab)
- [A4. Frequently Asked Questions (FAQ)](#a4-frequently-asked-questions-faq)
- [A5. Common Error Messages & Fixes](#a5-common-error-messages--fixes)
- [A6. Essential Package List (by Category)](#a6-essential-package-list-by-category)
- [A7. Backup, Restore & Uninstall Termux](#a7-backup-restore--uninstall-termux)
- [A8. Useful Aliases & One-Liner Commands](#a8-useful-aliases--one-liner-commands)
- [A9. Termux vs Other Options (Comparison)](#a9-termux-vs-other-options-comparison)
- [A10. One-Page Master Cheat Sheet](#a10-one-page-master-cheat-sheet)

---

## A1. Termux Directory Structure Explained

Termux apna poora "Linux system" ek sandboxed folder ke andar rakhta hai — asli Android system files ko touch nahi karta.

| Path | Kya hai |
|---|---|
| `$PREFIX` (= `/data/data/com.termux/files/usr`) | Termux ka "root" — yahi par saare installed packages, binaries, libraries hote hain |
| `$HOME` (= `/data/data/com.termux/files/home`) | Aapka personal home folder — jahan aap scripts/projects rakhte ho |
| `$PREFIX/bin` | Saare installed commands/binaries (jaise `python`, `git`) yahan hote hain |
| `$PREFIX/etc` | Configuration files |
| `$PREFIX/lib` | Shared libraries |
| `~/storage/` | `termux-setup-storage` ke baad banta hai — phone ki actual storage (Downloads, DCIM, etc.) se linked |
| `~/.termux/` | Termux ki apni settings — `termux.properties`, `font.ttf`, `colors.properties`, `boot/` scripts |
| `~/.bashrc` / `~/.zshrc` | Shell startup file — yahan aliases, exports likhte ho |
| `/sdcard/` | Direct nahi milta bina permission ke — isiliye `~/storage/` use karte hain |

**Important:** Termux uninstall/clear-data karne par `$HOME` aur `$PREFIX` dono delete ho jaate hain — isliye zaroori files ko `~/storage/downloads` (actual phone storage) me copy karke rakho.

```bash
echo $PREFIX
echo $HOME
```

---

## A2. Complete Keyboard & Editor Shortcuts

### Termux Terminal Gestures & Keys

| Action | Shortcut |
|---|---|
| Cancel running command | `Ctrl + C` (ya Volume Down + C) |
| Clear screen | `Ctrl + L` |
| Search command history | `Ctrl + R` phir type karo |
| Move to line start / end | `Ctrl + A` / `Ctrl + E` |
| Delete word backward | `Ctrl + W` |
| Suspend process (background) | `Ctrl + Z` (resume: `fg`) |
| Autocomplete file/command | `Tab` |
| Extra keys row (Esc, Tab, arrows) | Long-press terminal screen |
| Zoom terminal text | Pinch gesture |
| New session | Swipe from left edge → "+" |
| Switch sessions | Swipe from left edge |

### `nano` Full Shortcuts

| Key | Action |
|---|---|
| `Ctrl+O` | Save (Write Out) |
| `Ctrl+X` | Exit |
| `Ctrl+K` | Cut line |
| `Ctrl+U` | Paste (Uncut) |
| `Ctrl+W` | Search |
| `Ctrl+\` | Search & Replace |
| `Ctrl+G` | Help menu |
| `Ctrl+C` | Show cursor position |
| `Alt+U` | Undo |
| `Alt+E` | Redo |

### `vim` Full Shortcuts

| Key | Action |
|---|---|
| `i` | Insert mode |
| `Esc` | Normal/command mode |
| `dd` | Delete (cut) current line |
| `yy` | Copy (yank) line |
| `p` | Paste |
| `u` | Undo |
| `Ctrl+r` | Redo |
| `/text` + Enter | Search "text" |
| `n` / `N` | Next / previous search result |
| `:%s/old/new/g` | Replace all occurrences in file |
| `gg` / `G` | Go to top / bottom of file |
| `:w` | Save |
| `:q` | Quit |
| `:wq` or `ZZ` | Save & quit |
| `:q!` | Quit without saving |

### Customizing Extra Keys Row

`~/.termux/termux.properties` me:

```
extra-keys = [ \
  ['ESC','/','-','HOME','UP','END','PGUP'], \
  ['TAB','CTRL','ALT','LEFT','DOWN','RIGHT','PGDN'] \
]
```
Apply karne ke liye: `termux-reload-settings`

---

## A3. Glossary — Har Term Ka Matlab

| Term | Matlab (simple words me) |
|---|---|
| **Shell** | Wo program jo aapke commands leke unhe execute karta hai (Termux default: `bash`) |
| **Package** | Ek software/tool jo `pkg install` se milta hai |
| **Repository (repo)** | Server jahan se packages download hote hain |
| **Binary** | Ek executable program file |
| **Root** | Android ka full-access admin mode — Termux ko root ki zaroorat nahi |
| **Root directory `/`** | Linux file system ka sabse upar wala folder |
| **PATH** | Wo list jahan shell dhoondti hai ki koi command kahan hai |
| **Environment variable** | Ek naam-value pair jo pura system use kar sakta hai (jaise `$HOME`) |
| **Daemon/Service** | Background me chalne wala program (jaise SSH server) |
| **Repository clone** | GitHub se code apne device par copy karna |
| **Commit** | Git me ek "save point" changes ka |
| **Shell script** | `.sh` file jisme commands sequence me likhe hote hain, ek saath run karne ke liye |
| **Chroot / proot** | Ek isolated mini Linux environment ke andar dusra Linux chalane ka tarika (root ke bina proot use hota hai) |
| **API** | Do programs ke beech data exchange karne ka standard tarika |
| **Port** | Network communication ka ek "channel number" (jaise 8080, 22, 443) |
| **Localhost** | Aapka apna hi device (`127.0.0.1`) |

---

## A4. Frequently Asked Questions (FAQ)

**Q: Termux Play Store se install karu ya F-Droid se?**
A: Hamesha **F-Droid** ya GitHub Releases se. Play Store version 2021 se update band ho chuka hai aur bahut sare packages usme kaam nahi karte.

**Q: Termux ke liye root chahiye kya?**
A: Nahi. Termux bina root ke poora chalta hai. Root sirf kuch advanced/system-level tasks ke liye chahiye hota hai (optional).

**Q: Termux band karne se background scripts ruk jaate hain?**
A: Haan, agar `termux-wake-lock` use nahi kiya to Android battery-optimization ke wajah se app ko kill kar sakta hai. Long tasks ke liye `termux-wake-lock` chalao aur Android settings me Termux ko "battery optimization se exclude" karo.

**Q: `pkg` aur `apt` me kya farak hai?**
A: `pkg` `apt` ka hi ek wrapper hai jo Termux ke liye extra helpful defaults deta hai (jaise auto-mirror select karna). Dono almost same kaam karte hain.

**Q: Termux me Play Store ke apps chala sakte hain?**
A: Nahi, Termux Linux command-line environment hai, Android APKs ke liye nahi. Uske liye emulators/waydroid alag cheez hai.

**Q: Storage access nahi mil raha?**
A: `termux-setup-storage` chalao aur Android system permission popup me "Allow" dabao. Agar popup nahi aata, App Info → Permissions → Storage manually enable karo.

**Q: `python` install kiya but `pip` "command not found" bol raha hai?**
A: Naye Termux versions me `pip` `python` ke saath hi aata hai. `pkg install python` phir se try karo, ya `python -m ensurepip` chalao.

**Q: Termux se WhatsApp/Instagram automation kar sakte hain?**
A: Kuch limited automation (jaise notification reading via Termux:API) possible hai, lekin full automation Android ke security restrictions ki wajah se risky/unreliable hai aur apps ke Terms of Service todh sakta hai.

**Q: Ek se zyada Termux sessions kaise use karein?**
A: Left edge se swipe karo → naya session "+" se banao. Sessions ke beech switch karne ke liye phir se swipe karo.

**Q: Termux data kaise backup karein naye phone me?**
A: Neeche **A7. Backup, Restore & Uninstall** section dekho.

---

## A5. Common Error Messages & Fixes

| Error Message | Kyun aata hai | Fix |
|---|---|---|
| `E: Unable to locate package X` | Repo list outdated ya galat mirror | `pkg update` phir try karo; ya `termux-change-repo` |
| `Permission denied` | File executable nahi hai ya wrong ownership | `chmod +x file.sh` |
| `bash: command not found` | Package install nahi hai ya PATH me nahi | `pkg install <package>` |
| `No space left on device` | Storage full hai | `pkg clean`, `du -sh */` se bade folders dhundo aur delete karo |
| `Failed to connect... Connection refused` | Server chal nahi raha ya galat port | Confirm karo server run ho raha hai + sahi port use ho raha hai |
| `SyntaxError: invalid syntax` (Python) | Code me typo/indentation issue | Line number check karo jo error me diya gaya hai |
| `fatal: not a git repository` | Us folder me `git init`/`git clone` nahi hua | `git init` ya sahi folder me jao |
| `Unable to locate a Java Runtime` | Java installed nahi | `pkg install openjdk-17` |
| `env: 'python': No such file or directory` | Shebang line galat hai script me | Script me `#!/data/data/com.termux/files/usr/bin/bash` use karo, ya `bash script.sh` se run karo |
| `Read-only file system` | System folder me likhne ki koshish | `$HOME` ke andar hi kaam karo, system files edit mat karo |
| `Could not resolve host` | Internet/DNS issue | `ping 8.8.8.8` check karo; DNS ho to `ping google.com` try karo |
| `zip: not found` | zip package missing | `pkg install zip unzip` |

---

## A6. Essential Package List (by Category)

### 🛠️ Core Development
```bash
pkg install git clang make cmake python nodejs openjdk-17 golang rust ruby php
```

### 📝 Editors
```bash
pkg install nano vim neovim micro
```

### 🌐 Networking & Downloading
```bash
pkg install curl wget openssh nmap net-tools whois rsync
```

### 📦 Compression / Archives
```bash
pkg install zip unzip tar p7zip
```

### 🎨 Media & Utilities
```bash
pkg install ffmpeg imagemagick termux-api figlet cmatrix
```

### 📊 Data / Databases
```bash
pkg install sqlite mariadb jq
```

### 🖥️ Terminal Enhancements
```bash
pkg install zsh tmux htop tree ncdu neofetch
```

> Sab ek saath install karne ke liye upar wale sabhi commands chala do — ye almost ek complete dev environment bana dega.

---

## A7. Backup, Restore & Uninstall Termux

### Backup (naye phone me shift karne ke liye ya safety ke liye)

```bash
pkg install tar
cd /data/data/com.termux/files
tar -cvzf ~/storage/downloads/termux-backup.tar.gz home usr
```
Ye backup `Downloads` folder me save ho jaayega — waha se aap use cloud/PC me copy kar sakte ho.

### Restore (naye Termux install me)

```bash
cd /data/data/com.termux/files
tar -xvzf ~/storage/downloads/termux-backup.tar.gz -C /data/data/com.termux/files
```

### Clean Uninstall

1. Android **Settings → Apps → Termux → Uninstall**
2. Agar companion apps (Termux:API, Termux:Styling, etc.) use kiye the, unhe bhi separately uninstall karo
3. `~/storage/downloads/` me rakha backup delete **na** karo agar future me chahiye ho

### Resetting Termux (bina uninstall kiye)

```bash
# Sab kuch clear karke fresh start (dhyan se — ye sab delete kar dega)
rm -rf $HOME/*
```

---

## A8. Useful Aliases & One-Liner Commands

`~/.bashrc` me daalne ke liye ready-made aliases:

```bash
alias update='pkg update && pkg upgrade -y'
alias ll='ls -la'
alias cls='clear'
alias ..='cd ..'
alias ...='cd ../..'
alias myip='curl -s ifconfig.me'
alias serve='python -m http.server 8080'
alias gs='git status'
alias ga='git add .'
alias gc='git commit -m'
alias gp='git push'
alias diskusage='du -sh */ | sort -rh'
alias ports='netstat -tulnp'
alias weather='curl wttr.in'
```

Activate karne ke liye:
```bash
source ~/.bashrc
```

**Handy one-liners:**

```bash
# Apna public IP dekho
curl ifconfig.me

# System info nicely dikhao
pkg install neofetch && neofetch

# Kisi folder ka size dekho
du -sh foldername/

# Sabse bade 10 files dhoondo current folder me
find . -type f -exec du -h {} + | sort -rh | head -10

# Live weather terminal me
curl wttr.in
```

---

## A9. Termux vs Other Options (Comparison)

| Feature | Termux | UserLAnd | Termux:X11 | Cloud Shell (SSH to VPS) |
|---|---|---|---|---|
| Root chahiye? | ❌ Nahi | ❌ Nahi | ❌ Nahi | ❌ Nahi (remote hai) |
| Native performance | ✅ Fast | ⚠️ Thoda slow (extra layer) | ✅ Fast | Depends on VPS |
| Full GUI Desktop | ⚠️ VNC ke through | ✅ Built-in | ✅ Native X11 | ❌ (SSH-only usually) |
| Offline use | ✅ Haan | ✅ Haan | ✅ Haan | ❌ Internet chahiye |
| Setup difficulty | Easy | Easy | Medium | Medium (server rent karna padta hai) |
| Best for | Learning, scripting, dev | Full distro experience | GUI apps + dev | Production-grade hosting |

---

## A10. One-Page Master Cheat Sheet

```
NAVIGATION        pwd | ls -la | cd dir | cd .. | mkdir dir | rm -r dir
FILES             cat f | nano f | cp a b | mv a b | rm f | touch f
PERMISSIONS       chmod +x f | chmod 755 f | chown user f
PACKAGES          pkg update && pkg upgrade -y | pkg install x | pkg uninstall x
SEARCH/TEXT       grep "x" f | sed 's/a/b/g' f | awk '{print $1}' f | sort | uniq
ARCHIVE           tar -czvf out.tar.gz dir/ | tar -xvf out.tar | zip -r out.zip dir/
NETWORK           ping host | curl url | wget url | ssh user@host | scp f user@host:/path
MONITOR           ps aux | htop | df -h | du -sh dir/ | top
GIT               git clone url | git add . | git commit -m "msg" | git push | git pull
PYTHON            pkg install python | python file.py | pip install pkg
NODE              pkg install nodejs | node file.js | npm install pkg
TERMUX-API        termux-battery-status | termux-camera-photo f.jpg | termux-location
STORAGE           termux-setup-storage | cd ~/storage/downloads
WAKE LOCK         termux-wake-lock | termux-wake-unlock
BACKUP            tar -cvzf backup.tar.gz $HOME $PREFIX
```

---

### 🎯 Contribution

Isko apne repo me `COURSE.md` ya `LEARNING_PATH.md` ke साथ merge/replace kar sakte hain. README.md ke "Repository Navigation" table me ek row add kar dena:

```markdown
| [Zero to Hero Course](https://github.com/trmxvibs/termux-commands/blob/main/TERMUX_ZERO_TO_HERO.md) | Complete beginner → advanced course |
```
