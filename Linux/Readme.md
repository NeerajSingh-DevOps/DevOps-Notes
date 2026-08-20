Bilkul bhai ❤️ Linux ke liye bhi same **professional DevOps Notes repository style** rakhenge. Isme basic commands se lekar **users, permissions, processes, services, networking, SSH, storage, logs, package management, shell scripting, troubleshooting aur DevOps use-cases** tak cover hoga.

<div align="center">

# 🐧 Linux — Complete DevOps Notes

### Learn → Practice → Automate → Troubleshoot → Master 🚀

<img src="https://img.shields.io/badge/Linux-Operating_System-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/Bash-Scripting-121011?style=for-the-badge&logo=gnubash&logoColor=white" />
<img src="https://img.shields.io/badge/DevOps-Essentials-2496ED?style=for-the-badge" />
<img src="https://img.shields.io/badge/Cloud-AWS%20%7C%20Azure-orange?style=for-the-badge" />

<br/>

**Complete Linux learning repository by [Neeraj Singh](https://github.com/NeerajSingh-DevOps)**

📚 Concepts • 💻 Commands • 🔐 Security • 🌐 Networking • ⚙️ Administration • 🚀 DevOps

</div>

---

# 👋 About This Repository

Welcome to my **Linux & DevOps Notes** repository.

Linux is one of the most important foundations for a Cloud/DevOps Engineer.

This repository covers Linux from **beginner fundamentals to practical system administration and DevOps usage**.

The objective is not just to remember commands, but to understand:

> **What is happening → Why it happens → How to troubleshoot it → How to automate it.**

---

# 🎯 Linux Learning Philosophy

```text id="v1kz6m"
                    🐧 LINUX
                       │
             ┌─────────┴─────────┐
             ▼                   ▼
          Basics             File System
             │                   │
             ▼                   ▼
          Commands          Permissions
             │                   │
             ▼                   ▼
          Processes            Users
             │                   │
             └─────────┬─────────┘
                       ▼
                    Services
                       │
                       ▼
                   Networking
                       │
                       ▼
                 Shell Scripting
                       │
                       ▼
                  Automation
                       │
                       ▼
               🚀 DevOps / Cloud
```

---

# 📚 Table of Contents

- [🐧 What is Linux?](#-what-is-linux)
- [🏗️ Linux Architecture](#️-linux-architecture)
- [📁 Linux File System](#-linux-file-system)
- [💻 Basic Commands](#-basic-commands)
- [📂 File & Directory Management](#-file--directory-management)
- [🔍 Searching](#-searching)
- [📖 Viewing Files](#-viewing-files)
- [✏️ Text Processing](#️-text-processing)
- [🔐 Users & Groups](#-users--groups)
- [🛡️ Permissions](#️-permissions)
- [👑 sudo & Root](#-sudo--root)
- [⚙️ Processes](#️-processes)
- [🔄 Services](#-services)
- [📦 Package Management](#-package-management)
- [💾 Storage & Disk](#-storage--disk)
- [🌐 Networking](#-networking)
- [🔑 SSH](#-ssh)
- [📝 Logs](#-logs)
- [⏰ Cron Jobs](#-cron-jobs)
- [🐚 Bash Scripting](#-bash-scripting)
- [🔄 Pipes & Redirection](#-pipes--redirection)
- [📊 System Monitoring](#-system-monitoring)
- [🔧 Troubleshooting](#-troubleshooting)
- [🐳 Linux & Docker](#-linux--docker)
- [☁️ Linux & Cloud](#️-linux--cloud)
- [🚀 Linux in DevOps](#-linux-in-devops)
- [🧪 Hands-on Projects](#-hands-on-projects)
- [🎯 Interview Questions](#-interview-questions)
- [📋 Command Cheat Sheet](#-command-cheat-sheet)

---

# 🐧 What is Linux?

Linux is an open-source operating system kernel used in many operating systems and server environments.

Popular Linux distributions:

- Ubuntu
- Debian
- Red Hat Enterprise Linux
- Rocky Linux
- AlmaLinux
- Amazon Linux
- Fedora

---

# 🏗️ Linux Architecture

```text id="a9v6kr"
                 👤 User
                   │
                   ▼
              Applications
                   │
                   ▼
                 Shell
                   │
                   ▼
                Kernel
                   │
          ┌────────┼────────┐
          ▼        ▼        ▼
        CPU      Memory   Devices
                   │
                   ▼
                Hardware
```

### Important Components

| Component | Purpose |
|---|---|
| Kernel | Core of OS |
| Shell | Interface to OS |
| File System | Organizes data |
| Processes | Running programs |
| Users | Identities |
| Services | Background applications |

---

# 🏠 Linux File System

Linux follows a hierarchical file system.

```text id="g6hj93"
/ 
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── srv
├── sys
├── tmp
├── usr
└── var
```

---

# 📁 Important Directories

| Directory | Purpose |
|---|---|
| `/` | Root |
| `/home` | User home directories |
| `/root` | Root user's home |
| `/etc` | Configuration |
| `/var` | Variable data/logs |
| `/tmp` | Temporary files |
| `/usr` | User applications/libraries |
| `/bin` | Essential commands |
| `/sbin` | System administration commands |
| `/dev` | Device files |
| `/proc` | Process/kernel information |
| `/opt` | Optional software |

---

# 💻 Basic Commands

## Print Working Directory

```bash id="w6p3o0"
pwd
```

## List Files

```bash id="v3s3de"
ls
```

Detailed:

```bash id="p0c7pr"
ls -l
```

Hidden files:

```bash id="xq1xg8"
ls -la
```

## Change Directory

```bash id="2g1h8s"
cd /etc
```

Go back:

```bash id="6w5qkv"
cd ..
```

Home:

```bash id="7k1t8k"
cd ~
```

---

# 📂 File & Directory Management

Create directory:

```bash id="p5zv6w"
mkdir project
```

Create nested directories:

```bash id="d7y9ui"
mkdir -p project/src/app
```

Create file:

```bash id="w0z0iz"
touch file.txt
```

Copy:

```bash id="0e0x8v"
cp file.txt backup.txt
```

Copy directory:

```bash id="i9j3xq"
cp -r project project-backup
```

Move:

```bash id="w5iqp5"
mv file.txt /tmp/
```

Rename:

```bash id="u8z8y8"
mv old.txt new.txt
```

Delete file:

```bash id="s2u3bq"
rm file.txt
```

Delete directory:

```bash id="u0p2r5"
rm -r project
```

⚠️ Be extremely careful with recursive deletion.

---

# 🔍 Searching

Find files:

```bash id="q7q7r3"
find /var -name "*.log"
```

Search text:

```bash id="8ksjvn"
grep "error" application.log
```

Recursive search:

```bash id="tqf5e4"
grep -r "error" /var/log/
```

Find command location:

```bash id="lq3m3s"
which python
```

---

# 📖 Viewing Files

Display:

```bash id="w9qzqu"
cat file.txt
```

Read page by page:

```bash id="q3l9cv"
less file.txt
```

First lines:

```bash id="u0oy5g"
head file.txt
```

Last lines:

```bash id="7v6gq8"
tail file.txt
```

Live log monitoring:

```bash id="u2o8ji"
tail -f application.log
```

---

# ✏️ Text Processing

## grep

Search text:

```bash id="b0z9xj"
grep "ERROR" app.log
```

## awk

Process structured text:

```bash id="t7p6ar"
awk '{print $1}' access.log
```

## sed

Replace text:

```bash id="2j4qz4"
sed 's/old/new/g' file.txt
```

## sort

```bash id="l0yqgk"
sort file.txt
```

## uniq

```bash id="v6m9y1"
uniq file.txt
```

## wc

```bash id="j4s6ah"
wc -l file.txt
```

---

# 🔐 Users & Groups

Linux is a multi-user operating system.

```text id="wlm2e7"
Linux System
     │
 ┌───┼────────┐
 ▼   ▼        ▼
User User     User
 │
 ▼
Groups
```

List current user:

```bash id="z1h7oz"
whoami
```

User ID:

```bash id="8i9yhj"
id
```

List users:

```bash id="4zq6d8"
cat /etc/passwd
```

Create user:

```bash id="c1b0f0"
sudo useradd -m neeraj
```

Set password:

```bash id="p4a0o7"
sudo passwd neeraj
```

Create group:

```bash id="j6h9sx"
sudo groupadd devops
```

Add user to group:

```bash id="p6v7n3"
sudo usermod -aG devops neeraj
```

---

# 🛡️ Linux Permissions

Linux permissions:

```text id="y5v8g4"
r → Read
w → Write
x → Execute
```

Example:

```text id="7z4z1j"
-rwxr-xr--
```

Breakdown:

```text id="n2q1i7"
Owner   Group   Others
rwx     r-x     r--
```

---

# 🔢 Permission Numbers

| Permission | Value |
|---|---:|
| Read | 4 |
| Write | 2 |
| Execute | 1 |

Example:

```text id="b9y7v9"
7 = 4 + 2 + 1 = rwx
5 = 4 + 1     = r-x
4 = 4         = r--
```

Therefore:

```bash id="j2m8q3"
chmod 754 script.sh
```

---

# 🔧 chmod

Change permissions:

```bash id="0b6q6y"
chmod 755 script.sh
```

Add execute:

```bash id="9qf8jk"
chmod +x script.sh
```

---

# 👤 chown

Change ownership:

```bash id="8q2f6m"
sudo chown neeraj:devops file.txt
```

---

# 👑 sudo & Root

Root has extensive system privileges.

Check current user:

```bash id="c7q8c4"
whoami
```

Run command with elevated privileges:

```bash id="u1d3b6"
sudo command
```

Switch user:

```bash id="6k6t9a"
su - username
```

### Best Practice

> 🔐 Use least privilege and avoid working as root unnecessarily.

---

# ⚙️ Processes

A process is a running program.

View processes:

```bash id="3j8w8y"
ps
```

Detailed:

```bash id="5v2x3v"
ps aux
```

Real-time monitoring:

```bash id="8e6y2t"
top
```

Search process:

```bash id="c5k2e0"
ps aux | grep nginx
```

---

# 🛑 Kill Process

Find PID:

```bash id="5r8c5r"
ps aux | grep nginx
```

Terminate:

```bash id="0j9g4k"
kill <PID>
```

Force terminate:

```bash id="9d3t5w"
kill -9 <PID>
```

> ⚠️ Prefer graceful termination before using `kill -9`.

---

# 🔄 Services

Modern Linux distributions commonly use `systemd`.

Check service:

```bash id="j4f2n0"
systemctl status nginx
```

Start:

```bash id="8c7b7v"
sudo systemctl start nginx
```

Stop:

```bash id="4x9g4k"
sudo systemctl stop nginx
```

Restart:

```bash id="m7n1x2"
sudo systemctl restart nginx
```

Enable at boot:

```bash id="u5w2q0"
sudo systemctl enable nginx
```

---

# 📦 Package Management

## Ubuntu / Debian

Update package metadata:

```bash id="1j8k5c"
sudo apt update
```

Upgrade:

```bash id="x7m5q3"
sudo apt upgrade
```

Install:

```bash id="j4z1y4"
sudo apt install nginx
```

Remove:

```bash id="w7t2b9"
sudo apt remove nginx
```

---

## RHEL-based

```bash id="0r9x5h"
sudo dnf install nginx
```

Update:

```bash id="1n8k5h"
sudo dnf update
```

---

# 💾 Storage & Disk

Check disk space:

```bash id="q0s6g8"
df -h
```

Check directory size:

```bash id="7q5y6q"
du -sh /var/log
```

List block devices:

```bash id="2n7p6b"
lsblk
```

Mount filesystem:

```bash id="3g6x2d"
sudo mount /dev/sdb1 /mnt
```

Unmount:

```bash id="f7p8e3"
sudo umount /mnt
```

---

# 🌐 Networking

Show IP:

```bash id="c0q3r4"
ip addr
```

Show routes:

```bash id="6w9f7g"
ip route
```

Test connectivity:

```bash id="2j8y9u"
ping 8.8.8.8
```

DNS lookup:

```bash id="4f8w0a"
nslookup example.com
```

Or:

```bash id="j7p4n3"
dig example.com
```

Test HTTP:

```bash id="z7n5u4"
curl https://example.com
```

Download:

```bash id="6v0m9h"
wget https://example.com/file
```

---

# 🔑 SSH

SSH = Secure Shell.

Used to remotely connect to Linux servers.

```text id="o7t6u8"
Local Machine
     │
     │ SSH
     ▼
Linux Server
```

Connect:

```bash id="v9d4s8"
ssh username@server-ip
```

Using private key:

```bash id="m3w6x8"
ssh -i key.pem username@server-ip
```

---

# 🔐 SSH Key Authentication

```text id="v4h1j7"
Client
 │
 ├── Private Key 🔑
 │
 ▼
SSH Server
 │
 └── Public Key
```

Generate key:

```bash id="f3y6t1"
ssh-keygen -t ed25519
```

Test:

```bash id="d2h5x7"
ssh -T git@github.com
```

---

# 📝 Linux Logs

Important logs are commonly under:

```text id="c4n8t6"
/var/log/
```

View:

```bash id="3f5j9k"
ls /var/log/
```

Follow a log:

```bash id="p9y3v7"
tail -f /var/log/syslog
```

On systemd systems:

```bash id="j7u5e8"
journalctl
```

Service logs:

```bash id="e3z6s4"
journalctl -u nginx
```

---

# ⏰ Cron Jobs

Cron schedules recurring tasks.

Edit cron:

```bash id="x9m2b8"
crontab -e
```

List:

```bash id="k5q7w3"
crontab -l
```

Example:

```text id="y3s8w4"
0 2 * * * /home/neeraj/backup.sh
```

Meaning:

```text id="h1k9p4"
02:00 every day
```

---

# 🐚 Bash Scripting

Bash allows Linux tasks to be automated.

Basic script:

```bash id="z6x4b1"
#!/bin/bash

echo "Hello DevOps"
```

Make executable:

```bash id="x5m3a7"
chmod +x script.sh
```

Run:

```bash id="g4n8k2"
./script.sh
```

---

# 🔢 Variables

```bash id="y4f8m6"
NAME="Neeraj"

echo "Hello $NAME"
```

---

# 🔀 Conditions

```bash id="w9j2s6"
if [ "$ENV" = "prod" ]; then
    echo "Production"
else
    echo "Non-Production"
fi
```

---

# 🔁 Loops

```bash id="a5r3n7"
for file in *.log
do
    echo "$file"
done
```

---

# 🧩 Functions

```bash id="p7q8d1"
check_service() {
    systemctl status nginx
}

check_service
```

---

# 🔄 Pipes & Redirection

## Pipe

```bash id="r3x7m5"
ps aux | grep nginx
```

Pipe sends output from one command to another.

---

## Output Redirection

```bash id="n8k4p2"
echo "Hello" > file.txt
```

Append:

```bash id="m5v9c3"
echo "Another line" >> file.txt
```

Error redirection:

```bash id="z4x6b8"
command 2> error.log
```

Both output and errors:

```bash id="h8p3q6"
command > output.log 2>&1
```

---

# 📊 System Monitoring

CPU:

```bash id="g2s8w5"
top
```

Memory:

```bash id="n7c4m2"
free -h
```

Disk:

```bash id="j5q9v1"
df -h
```

Processes:

```bash id="t8x3b7"
ps aux
```

Uptime:

```bash id="f6r2y8"
uptime
```

Load:

```bash id="c5m7p4"
uptime
```

---

# 🔧 Linux Troubleshooting Framework

When a server has an issue:

```text id="s5x8j1"
              🚨 Problem
                  │
                  ▼
             Check Status
                  │
                  ▼
              Check Logs
                  │
                  ▼
            Check Processes
                  │
                  ▼
            Check Resources
          ┌───────┼────────┐
          ▼       ▼        ▼
         CPU     RAM      Disk
                  │
                  ▼
             Networking
                  │
                  ▼
            Configuration
                  │
                  ▼
               Fix
                  │
                  ▼
             Verify Again
```

---

# 🚨 Common Troubleshooting Commands

### Service not working

```bash id="y5t8c3"
systemctl status nginx
journalctl -u nginx
```

### Disk full

```bash id="q7r3w5"
df -h
du -sh /*
```

### High CPU

```bash id="g9m2x6"
top
ps aux --sort=-%cpu
```

### High Memory

```bash id="f4k7z9"
free -h
ps aux --sort=-%mem
```

### Network issue

```bash id="n3v8c1"
ip addr
ip route
ping <IP>
curl <URL>
```

### Port issue

```bash id="b6y2m8"
ss -tulpn
```

---

# 🐳 Linux & Docker

Docker runs containers using Linux kernel capabilities.

```text id="s1v5x8"
Linux Host
    │
    ▼
 Docker
    │
 ┌──┼──────┐
 ▼  ▼      ▼
App DB   Nginx
Containerized Workloads
```

Useful commands:

```bash id="d8m4q2"
docker ps
docker images
docker logs <container>
docker exec -it <container> /bin/bash
```

---

# ☁️ Linux & Cloud

Linux is widely used in cloud environments.

Typical AWS workflow:

```text id="x4k7p9"
AWS
 │
 ▼
EC2
 │
 ▼
Linux
 │
 ├── SSH
 ├── Nginx
 ├── Docker
 ├── Git
 ├── Terraform
 └── Application
```

---

# 🚀 Linux in DevOps

Linux connects almost every major DevOps tool:

```text id="p8y2m6"
                   🐧 Linux
                      │
        ┌─────────────┼─────────────┐
        ▼             ▼             ▼
       Git          Docker       Terraform
        │             │             │
        ▼             ▼             ▼
     GitHub          ECR           AWS
        │             │             │
        └─────────────┼─────────────┘
                      ▼
                    CI/CD
                      │
                      ▼
                 Kubernetes
                      │
                      ▼
                 🚀 Production
```

---

# 🧪 Hands-on Projects

## 🚀 Project 01 — Linux User Management

Practice:

```text id="o7j4p3"
Create Users
      ↓
Create Groups
      ↓
Assign Permissions
      ↓
Test Access
```

---

## 🚀 Project 02 — Web Server

Install Nginx:

```bash id="v4y9m2"
sudo apt update
sudo apt install nginx
```

Start:

```bash id="z5k8q1"
sudo systemctl start nginx
```

Verify:

```bash id="p2r6x7"
curl localhost
```

---

## 🚀 Project 03 — Linux Monitoring Script

Create a Bash script that checks:

- CPU usage
- Memory usage
- Disk usage
- Service status

```text id="e8s2n5"
Monitoring Script
      │
 ┌────┼────┐
 ▼    ▼    ▼
CPU  RAM  Disk
      │
      ▼
   Alert
```

---

## 🚀 Project 04 — Automated Backup

```text id="c7x4m8"
Cron
 ↓
Backup Script
 ↓
Compress Files
 ↓
Store Backup
 ↓
Log Result
```

---

## 🚀 Project 05 — Linux + Docker

```text id="f9r3w6"
Linux VM
   ↓
Docker
   ↓
Container
   ↓
Nginx
   ↓
Application
```

---

# 🎯 Linux Interview Questions

## 🐧 Fundamentals

- What is Linux?
- Linux vs Unix?
- What is a kernel?
- What is a shell?
- What is Bash?
- What is a process?

## 📁 File System

- Explain Linux file system hierarchy.
- `/etc` vs `/var`?
- `/home` vs `/root`?
- What is `/proc`?

## 🔐 Permissions

- What is `chmod`?
- What is `chown`?
- Explain `755`.
- Explain `rwxr-xr--`.
- User vs Group vs Others?

## ⚙️ Processes

- What is PID?
- How do you find a process?
- How do you kill a process?
- `kill` vs `kill -9`?

## 🔄 Services

- What is systemd?
- `start` vs `enable`?
- How do you troubleshoot a failed service?

## 🌐 Networking

- How do you find IP?
- How do you check routes?
- How do you check listening ports?
- What is DNS?
- What is SSH?

## 🐚 Bash

- What is shell scripting?
- Variables?
- Conditions?
- Loops?
- Functions?
- Cron jobs?

---

# 📋 Linux Command Cheat Sheet

| Category | Command | Purpose |
|---|---|---|
| Navigation | `pwd` | Current directory |
| Navigation | `ls` | List files |
| Navigation | `cd` | Change directory |
| Files | `touch` | Create file |
| Files | `cp` | Copy |
| Files | `mv` | Move/Rename |
| Files | `rm` | Remove |
| Directory | `mkdir` | Create directory |
| Search | `find` | Find files |
| Search | `grep` | Search text |
| Text | `awk` | Text processing |
| Text | `sed` | Stream editing |
| Text | `sort` | Sort output |
| Text | `wc` | Count |
| Users | `whoami` | Current user |
| Users | `id` | User/group IDs |
| Users | `useradd` | Create user |
| Permissions | `chmod` | Change permissions |
| Permissions | `chown` | Change ownership |
| Process | `ps` | Processes |
| Process | `top` | Live monitoring |
| Process | `kill` | Stop process |
| Service | `systemctl` | Manage services |
| Disk | `df` | Disk space |
| Disk | `du` | Directory size |
| Disk | `lsblk` | Block devices |
| Network | `ip` | Network config |
| Network | `ss` | Sockets/ports |
| Network | `curl` | HTTP requests |
| Network | `ping` | Connectivity |
| SSH | `ssh` | Remote login |
| Logs | `journalctl` | System logs |
| Schedule | `crontab` | Scheduled jobs |

---

# 🧠 Linux Mental Model

Remember Linux like this:

```text id="s7m4x2"
                    🐧 Linux
                       │
             ┌─────────┴─────────┐
             ▼                   ▼
          Kernel                Shell
             │                   │
             ▼                   ▼
         Hardware            Commands
                                 │
                    ┌────────────┼────────────┐
                    ▼            ▼            ▼
                  Files       Processes     Network
                    │            │            │
                    ▼            ▼            ▼
               Permissions    Services       SSH
                    │            │            │
                    └────────────┼────────────┘
                                 ▼
                         🐚 Automation
                                 │
                                 ▼
                           🚀 DevOps
```

---

# 🏆 Linux Learning Path

```text id="x3n7q9"
Linux Basics
      ↓
File System
      ↓
Commands
      ↓
Users & Groups
      ↓
Permissions
      ↓
Processes
      ↓
Services
      ↓
Storage
      ↓
Networking
      ↓
SSH
      ↓
Logs
      ↓
Cron
      ↓
Bash Scripting
      ↓
Troubleshooting
      ↓
Docker
      ↓
Cloud
      ↓
CI/CD
      ↓
🚀 DevOps Engineer
```

---

# 📁 Recommended Repository Structure

```text id="r8k5m1"
Linux-Notes/
│
├── README.md
│
├── 01-Linux-Basics/
│   ├── Introduction.md
│   ├── Architecture.md
│   └── Distributions.md
│
├── 02-File-System/
│   ├── Linux-Directories.md
│   └── File-Management.md
│
├── 03-Commands/
│   ├── Basic-Commands.md
│   ├── Search.md
│   └── Text-Processing.md
│
├── 04-Users-Permissions/
│   ├── Users.md
│   ├── Groups.md
│   └── Permissions.md
│
├── 05-Processes-Services/
│   ├── Processes.md
│   └── Systemd.md
│
├── 06-Storage/
│   ├── Disk.md
│   └── Mounting.md
│
├── 07-Networking/
│   ├── Networking.md
│   ├── SSH.md
│   └── DNS.md
│
├── 08-Logs/
│   └── Linux-Logs.md
│
├── 09-Cron/
│   └── Cron-Jobs.md
│
├── 10-Bash/
│   ├── Variables.md
│   ├── Conditions.md
│   ├── Loops.md
│   └── Scripts.md
│
├── 11-Troubleshooting/
│   └── Troubleshooting.md
│
├── 12-DevOps/
│   ├── Docker.md
│   ├── Git.md
│   └── Cloud.md
│
└── 13-Projects/
    ├── Web-Server/
    ├── Monitoring-Script/
    ├── Backup-Automation/
    └── Docker-Lab/
```

---

# 🛠️ Tech Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=linux,bash,git,github,docker,terraform,aws,azure,kubernetes" />

<br/><br/>

<img src="https://img.shields.io/badge/Linux-System%20Administration-FCC624?style=flat-square&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/Bash-Automation-121011?style=flat-square&logo=gnubash&logoColor=white" />
<img src="https://img.shields.io/badge/Git-Version%20Control-F05032?style=flat-square&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-Containers-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Terraform-IaC-844FBA?style=flat-square&logo=terraform&logoColor=white" />

</div>

---

# 👨‍💻 About Me

<div align="center">

### Neeraj Singh

**Cloud & DevOps Engineer | AWS | Azure | Terraform | Linux | Docker | Kubernetes**

I'm building my Cloud & DevOps engineering skills through hands-on infrastructure, automation and troubleshooting.

Linux is one of the core foundations of my DevOps learning journey, and this repository documents the commands, concepts and practical labs I use along the way.

</div>

---

# 🤝 Connect With Me

<div align="center">

<a href="https://github.com/NeerajSingh-DevOps">
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="https://www.linkedin.com/in/NeerajSingh-DevOps">
<img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

</div>

---

<div align="center">

### 🐧 Linux → 🐙 Git → 🐳 Docker → 🏗️ Terraform → ☁️ AWS/Azure → ☸️ Kubernetes → 🚀 DevOps

**Learn it. Practice it. Automate it. Troubleshoot it. Master it. 🔥**

⭐ **If these notes help you, consider starring the repository!**

<br/>

<i>Strong DevOps starts with strong fundamentals — and Linux is one of them. 🐧🚀</i>

</div>
