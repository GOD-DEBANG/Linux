# 🐧 Linux Zero-to-Hero Cheat Sheet

A comprehensive reference for learning Linux from **absolute beginner** to **advanced**.

## 📖 Table of Contents
1. [Basics](#-1-basics)
2. [File & Directory Management](#-2-file--directory-management)
3. [Permissions](#-3-permissions)
4. [Searching & Disk Usage](#-4-searching--disk-usage)
5. [Package Management](#-5-package-management)
6. [Process & System Monitoring](#-6-process--system-monitoring)
7. [Networking](#-7-networking)
8. [Users & Groups](#-8-users--groups)
9. [Archiving & Compression](#-9-archiving--compression)
10. [Bash Scripting](#-10-bash-scripting)
11. [Automation with Cron](#-11-automation-with-cron)
12. [Security & Firewall](#-12-security--firewall)
13. [Performance & Logs](#-13-performance--logs)
14. [Containers & Virtualization](#-14-containers--virtualization)
15. [Advanced Shell Tricks](#-15-advanced-shell-tricks)
16. [Learning Roadmap](#-16-learning-roadmap)

## 🐣 1. Basics
| Command      | Description                  |
|---------------|----------------------------|
| `pwd`         | Print working directory     |
| `ls -l`       | List files with details     |
| `cd /path`    | Change directory            |
| `cd ~`        | Home directory              |
| `date`        | Show current date/time      |
| `clear`       | Clear terminal screen       |
| `man cmd`     | Manual for a command        |
| `history`     | Show command history        |

## 📂 2. File & Directory Management
| Command                | Description                |
|------------------------|---------------------------|
| `touch file`           | Create file               |
| `mkdir dir`            | Create directory          |
| `rm file`              | Delete file               |
| `rm -r dir`            | Delete directory          |
| `cp file dest`         | Copy file                 |
| `mv file dest`         | Move or rename file       |
| `cat file`             | View file content         |
| `head -n 10 file`      | First 10 lines            |
| `tail -n 10 file`      | Last 10 lines             |
| `tree`                 | Show directory tree       |

## 🔑 3. Permissions
| Command                     | Description                  |
|-----------------------------|------------------------------|
| `chmod 755 file`            | Change permissions           |
| `chown user:group file`     | Change owner and group       |
| `umask`                     | Show/set default permissions |

## 🔎 4. Searching & Disk Usage
| Command                       | Description            |
|-------------------------------|------------------------|
| `find /path -name "*.txt"`    | Find files by name     |
| `locate filename`             | Locate files quickly   |
| `grep "word" file`            | Search in file         |
| `du -sh *`                    | Disk usage summary     |
| `df -h`                       | Disk space usage       |

## 📦 5. Package Management
**Debian/Ubuntu:**
```
sudo apt update
sudo apt install package
sudo apt remove package
```
**RHEL/Fedora:**
```
sudo dnf install package
sudo dnf remove package
sudo dnf upgrade
```

## ⚙ 6. Process & System Monitoring
| Command    | Description            |
|------------|----------------------|
| `ps aux`   | Show processes       |
| `top`/`htop`| Real-time monitor   |
| `kill PID` | Kill process         |
| `uptime`   | System uptime        |
| `free -h`  | Memory usage         |
| `uname -a` | System info         |

## 🌐 7. Networking
| Command            | Description              |
|--------------------|------------------------|
| `ping host`        | Test connectivity       |
| `ip a`             | Show interfaces         |
| `netstat -tulnp`   | Show open ports         |
| `ssh user@host`    | SSH login               |
| `scp file user@h:/`| Secure copy             |
| `curl URL`         | Fetch data              |

## 👥 8. Users & Groups
| Command                  | Description             |
|--------------------------|------------------------|
| `whoami`                 | Current user           |
| `sudo adduser name`      | Add new user           |
| `passwd name`            | Change password        |
| `groups`                 | Show groups            |
| `sudo userdel name`      | Delete user            |

## 🗜 9. Archiving & Compression
| Command                     | Description        |
|-----------------------------|-------------------|
| `tar -cvf file.tar dir`     | Create tar         |
| `tar -xvf file.tar`         | Extract tar        |
| `gzip file`                 | Gzip compress      |
| `gunzip file.gz`            | Gzip decompress    |
| `zip -r file.zip dir`       | Create zip         |
| `unzip file.zip`            | Extract zip        |

## 💻 10. Bash Scripting
```bash
#!/bin/bash
NAME="Linux"
echo "Hello $NAME"

# If-Else
if [ -f "file.txt" ]; then
  echo "File exists"
else
  echo "File not found"
fi

# Loop
for i in {1..5}; do
  echo "Count: $i"
done

# Function
greet() {
  echo "Welcome, $1"
}
greet "User"
```

## ⏰ 11. Automation with Cron
| Command       | Description                  |
|----------------|----------------------------|
| `crontab -e`  | Edit cron jobs              |
| `crontab -l`  | List cron jobs              |
| Example: `0 2 * * * /path/script.sh` → Run daily at 2AM |

## 🔒 12. Security & Firewall
| Command              | Description            |
|----------------------|----------------------|
| `ufw enable`         | Enable firewall      |
| `ufw allow 22`       | Allow SSH           |
| `ssh-keygen -t rsa`  | Generate SSH keys   |
| `chmod 600 key.pem`  | Secure key file     |

## 📊 13. Performance & Logs
| Command          | Description            |
|------------------|----------------------|
| `vmstat 1`       | View system stats    |
| `journalctl -xe` | View logs            |
| `iotop`          | Monitor disk I/O     |
| `dmesg | less`   | Kernel messages      |

## 🐳 14. Containers & Virtualization
| Command                  | Description           |
|--------------------------|----------------------|
| `docker ps`              | List containers      |
| `docker run -it ubuntu`  | Run Ubuntu container |
| `virt-manager`           | Manage VMs GUI      |

## ⚡ 15. Advanced Shell Tricks
| Feature              | Example                |
|----------------------|-----------------------|
| Command substitution | `VAR=$(ls)`           |
| Brace expansion      | `touch file{1..5}.txt`|
| Background job       | `command &`           |
| Search history       | `Ctrl + R`            |

## 🧭 16. Learning Roadmap
1. Week 1–2: Basics, navigation, file ops.  
2. Week 3–4: Permissions, search, editing.  
3. Week 5–6: Scripting, package mgmt.  
4. Week 7–8: Networking, SSH, cron.  
5. Week 9–10: Logs, monitoring, security.  
6. Beyond: Docker, kernel tuning, automation tools.

> ✅ **Tip:** Use `man` or `--help` with any command for detailed usage. Practice on a virtual machine or WSL before making changes on a production system.
