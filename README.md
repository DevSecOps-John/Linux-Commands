# 🐧 Linux Commands for DevSecOps 

<div align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/a/af/Tux.png" width="180"/>

# 🚀 Linux Complete Commands Guide

### Beginner to Advanced Linux Commands
### DevOps | Cloud | AWS | Kubernetes | System Administration

![Linux](https://img.shields.io/badge/Linux-Commands-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge&logo=amazonaws)
![DevOps](https://img.shields.io/badge/DevOps-Automation-blue?style=for-the-badge)
![Shell](https://img.shields.io/badge/Shell-Scripting-green?style=for-the-badge)

</div>

---

# 📘 Table of Contents

1. [Linux Basics](#1-linux-basics)
2. [File Management](#2-file-management-commands)
3. [Navigation Commands](#3-navigation-commands)
4. [User Management](#4-user-management)
5. [Permissions](#5-permissions-management)
6. [Process Management](#6-process-management)
7. [Package Management](#7-package-management)
8. [Networking Commands](#8-networking-commands)
9. [Storage Commands](#9-storage-commands)
10. [AWS EBS & EFS](#10-aws-ebs--efs)
11. [System Monitoring](#11-system-monitoring)
12. [Service Management](#12-service-management)
13. [Shell Scripting](#13-shell-scripting)
14. [Compression Commands](#14-compression-commands)
15. [Logging & Auditing](#15-logging--auditing)
16. [Docker Commands](#16-docker-commands)
17. [Git Commands](#17-git-commands)
18. [SSH & Security](#18-ssh--security)
19. [Useful DevOps Commands](#19-useful-devops-commands)

---

# 🐧 1. Linux Basics

| Command | Description |
|---------|-------------|
| `sudo su -` | Switch to root user |
| `su - username` | Switch user |
| `pwd` | Present working directory |
| `whoami` | Current logged in user |
| `hostname` | Show server hostname |
| `clear` | Clear terminal screen |
| `history` | Show command history |

---

# 📂 2. File Management Commands

| Command | Description |
|---------|-------------|
| `touch file` | Create file |
| `mkdir dir` | Create directory |
| `rm -rf file` | Remove file/directory |
| `cp file1 file2` | Copy file |
| `mv old new` | Move/Rename file |
| `cat file` | Read file |
| `cat > file` | Override content |
| `cat >> file` | Append content |
| `echo "hi"` | Print statement |
| `tree` | Show folder structure |
| `find / -name file` | Search file |
| `grep "text" file` | Filter content |

---

# 📁 3. Navigation Commands

| Command | Description |
|---------|-------------|
| `cd` | Change directory |
| `cd ..` | One step back |
| `cd ../..` | Two steps back |
| `cd ../../..` | Three steps back |
| `cd ~` | Home directory |
| `ls` | List files |
| `ls -l` | Detailed list |
| `ls -la` | Include hidden files |

---

# 👤 4. User Management

| Command | Description |
|---------|-------------|
| `useradd user1` | Create user |
| `passwd user1` | Set password |
| `id user1` | User details |
| `who` | Logged in users |
| `w` | Active users |
| `cat /etc/passwd` | User list |
| `cat /etc/group` | Group list |
| `userdel -r user1` | Delete user |
| `usermod -aG sudo user` | Add user to sudo group |
| `groups username` | Show user groups |

---

# 🔐 5. Permissions Management

## Permission Numbers

| Permission | Value |
|------------|-------|
| Read | 4 |
| Write | 2 |
| Execute | 1 |

```text
7 = Read + Write + Execute (4+2+1)
6 = Read + Write           (4+2)
5 = Read + Execute         (4+1)
4 = Read only              (4)
```

| Command | Description |
|---------|-------------|
| `chmod 777 file` | Full permissions |
| `chmod 755 file` | Standard permission |
| `chmod -R 755 dir` | Recursive permission |
| `chown user:group file` | Change ownership |

---

# ⚙️ 6. Process Management

| Command | Description |
|---------|-------------|
| `ps aux` | Detailed process list |
| `ps -ef` | All processes |
| `top` | CPU & RAM usage |
| `htop` | Interactive monitor |
| `top -u user` | User process |
| `kill -9 PID` | Force kill process |
| `pkill nginx` | Kill by name |
| `jobs` | Background jobs |
| `bg` | Resume in background |
| `fg` | Bring to foreground |
| `nohup command &` | Run after logout |

---

# 📦 7. Package Management

## YUM Commands (CentOS/RHEL)

| Command | Description |
|---------|-------------|
| `yum repolist` | Enabled repos |
| `yum list installed` | Installed packages |
| `yum search nginx` | Search package |
| `yum install nginx -y` | Install package |
| `yum remove nginx` | Remove package |
| `yum update -y` | Update system |

## APT Commands (Ubuntu/Debian)

| Command | Description |
|---------|-------------|
| `apt update` | Update repo list |
| `apt upgrade -y` | Upgrade packages |
| `apt install nginx -y` | Install package |
| `apt remove nginx` | Remove package |

---

# 🌐 8. Networking Commands

| Command | Description |
|---------|-------------|
| `curl ifconfig.me` | Public IP |
| `hostname -I` | Private IP |
| `ip a` | Show IP address |
| `ip addr show` | Network interfaces |
| `ss -tuln` | Open ports |
| `netstat -tulnp` | Show open ports |
| `ping google.com` | Test connectivity |
| `telnet IP PORT` | Test port |
| `nc -zv IP PORT` | Netcat port test |
| `traceroute google.com` | Route trace |
| `nslookup google.com` | DNS lookup |
| `dig google.com` | Advanced DNS |
| `curl -I https://example.com` | Check HTTP response |
| `wget https://url/file` | Download file |
| `ssh user@192.168.1.1` | Connect via SSH |
| `scp file.txt user@server:/path` | Copy file via SSH |

## NMAP Commands

```bash
# Scan common ports
nmap <target-ip>

# Scan specific ports
nmap -p 22,80 <target-ip>

# Scan all ports
nmap -p- <target-ip>
```

Example Output:

```text
22/tcp open   ssh
80/tcp open   http
```

---

# 💾 9. Storage Commands

| Command | Description |
|---------|-------------|
| `lsblk` | List block devices |
| `df -h` | Disk space usage |
| `du -sh *` | Folder size |
| `du -sh folder/` | Specific folder size |
| `mount` | Mounted filesystems |
| `umount /mnt/data` | Unmount disk |
| `file -s /dev/xvdf` | Check format |
| `mkfs.ext4 /dev/xvdf` | Format disk |
| `free -h` | Memory usage |
| `fdisk -l` | List disk partitions |

---

# ☁️ 10. AWS EBS & EFS

## 📀 EBS Commands

```bash
# Format Volume
mkfs.ext4 /dev/xvdb

# Mount Volume
mount /dev/xvdb /mnt/data

# Resize Volume (ext4)
growpart /dev/xvda 1

# Resize Volume (xfs)
xfs_growfs /dev/xvda1
```

> **Note:** Increasing the volume in AWS Console only enlarges the virtual disk.
> You must resize the partition and filesystem separately.

## 📂 EFS Commands

```bash
# Install EFS Utils
yum install -y amazon-efs-utils

# Create Mount Point
mkdir -p /mnt/efs

# Mount EFS
mount -t efs fs-xxxx:/ /mnt/efs
```

## 📊 EBS vs EFS

| Feature | EBS | EFS |
|---------|-----|-----|
| Type | Block Storage | File Storage |
| Access | Single EC2 | Multiple EC2 |
| Performance | High IOPS | Shared throughput |
| AZ Support | Single AZ | Multi AZ |
| Use Case | Databases | Shared Storage |

---

# 📈 11. System Monitoring

| Command | Description |
|---------|-------------|
| `uptime` | System uptime |
| `free -h` | RAM usage |
| `lscpu` | CPU details |
| `htop` | Interactive monitoring |
| `iostat -x 1` | Disk IO stats |
| `iftop` | Network traffic |
| `last reboot` | Reboot history |
| `journalctl -xe` | System logs |
| `dmesg` | Kernel messages |
| `last` | Last logins |

---

# 🧰 12. Service Management

| Command | Description |
|---------|-------------|
| `systemctl status nginx` | Check service status |
| `systemctl start nginx` | Start service |
| `systemctl stop nginx` | Stop service |
| `systemctl restart nginx` | Restart service |
| `systemctl enable nginx` | Auto-start on boot |
| `systemctl disable nginx` | Disable auto-start |
| `systemctl list-units` | List all services |
| `journalctl -u nginx` | View service logs |
| `journalctl -f` | Live system journal |
| `journalctl --since "1 hour ago"` | Recent logs |

---

# 📜 13. Shell Scripting

## Shebang Line

```bash
#!/bin/bash
```

## Run Script

```bash
# Method 1
sh test.sh

# Method 2
chmod +x test.sh
./test.sh
```

## Example Script

```bash
#!/bin/bash

echo "Welcome to Linux DevOps"
date
hostname
whoami
uptime
```

## Variables & Conditions

```bash
#!/bin/bash

# Variables
NAME="DevOps"
echo "Hello $NAME"

# If condition
if [ -f "/etc/nginx/nginx.conf" ]; then
  echo "Nginx config exists"
else
  echo "Nginx not found"
fi

# Loop
for i in 1 2 3; do
  echo "Count: $i"
done
```

---

# 🗜️ 14. Compression Commands

| Command | Description |
|---------|-------------|
| `tar -cvf archive.tar files/` | Create tar |
| `tar -xvf archive.tar` | Extract tar |
| `tar -czvf archive.tar.gz files/` | Create compressed tar |
| `tar -xzvf archive.tar.gz` | Extract compressed tar |
| `gzip file.txt` | Compress file |
| `gunzip file.txt.gz` | Decompress file |
| `zip -r archive.zip folder/` | Create zip |
| `unzip archive.zip` | Extract zip |

---

# 📄 15. Logging & Auditing

| Command | Description |
|---------|-------------|
| `tail -f /var/log/nginx/access.log` | Live log view |
| `cat /var/log/syslog` | System log |
| `journalctl -u nginx` | Service logs |
| `dmesg` | Kernel logs |
| `cat /var/log/secure` | Authentication logs |
| `grep "error" /var/log/messages` | Search logs |

---

# 🐳 16. Docker Commands

| Command | Description |
|---------|-------------|
| `docker ps` | Running containers |
| `docker ps -a` | All containers |
| `docker images` | List images |
| `docker build -t myapp .` | Build image |
| `docker run -d -p 80:80 nginx` | Run container |
| `docker stop container_id` | Stop container |
| `docker rm container_id` | Remove container |
| `docker logs container_id` | View logs |
| `docker exec -it container bash` | Enter container |
| `docker-compose up -d` | Start all services |
| `docker-compose down` | Stop all services |

---

# 🔁 17. Git Commands

| Command | Description |
|---------|-------------|
| `git init` | Initialize repo |
| `git clone https://github.com/...` | Clone repo |
| `git status` | Check changes |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Commit changes |
| `git push origin main` | Push to GitHub |
| `git pull origin main` | Pull latest changes |
| `git branch` | List branches |
| `git checkout -b new-branch` | Create new branch |
| `git merge branch-name` | Merge branch |

---

# 🔐 18. SSH & Security

| Command | Description |
|---------|-------------|
| `ssh-keygen -t rsa` | Generate SSH key |
| `ssh-copy-id user@server` | Copy key to server |
| `cat ~/.ssh/id_rsa.pub` | View public key |
| `ufw status` | Firewall status |
| `ufw allow 80/tcp` | Allow port 80 |
| `ufw enable` | Enable firewall |
| `ufw deny 22` | Block SSH port |
| `fail2ban-client status` | Check fail2ban |

---

# 🚀 19. Useful Tshoot DevOps Commands

| Command | Description |
|---------|-------------|
| `sudo netstat -tulnp` | Check Listening Ports Inside EC2 |
| `sudo ss -tulnp | grep 80` | Filter and check if a service is running |
| `curl -I http://localhost:80` | test locally If a web server is running, you’ll see HTTP headers|

| `docker ps` | Running containers |
| `aws s3 ls` | AWS S3 buckets |
| `terraform init` | Terraform initialize |
| `terraform plan` | Terraform plan |
| `terraform apply` | Terraform apply |
| `git status` | Git status |
| `helm list` | Helm releases |
| `ansible --version` | Ansible version |

---
# 🚀 20. Useful DevOps Installation Commands

Install a web server (Apache or Nginx):
sudo yum install -y httpd   # Amazon Linux
sudo systemctl enable httpd
sudo systemctl start httpd

or for Nginx:
sudo amazon-linux-extras enable nginx1
sudo yum install -y nginx
sudo systemctl enable nginx
sudo systemctl start nginx

Checklist for Apache/NGNIX on Amazon Linux 2023
Verify service status: Look for Active: active (running)
sudo systemctl status httpd

---

# 📸 Linux Architecture

```text
                    User
                      │
                      ▼
                Linux Shell
                      │
                      ▼
                  Kernel
                      │
       ┌──────────────┼──────────────┐
       ▼              ▼              ▼

   Process         Memory         Storage
  Management      Management     Management
```

---

# 🎯 Best Practices

- Use least privilege permissions
- Avoid `chmod 777` in production
- Monitor disk usage regularly
- Use SSH keys instead of passwords
- Keep systems updated
- Monitor logs frequently
- Always backup before major changes
- Use version control for all scripts

---

# ⭐ Support

If this repository helps you:

⭐ Star the repository
🍴 Fork the repository
📢 Share with others

---

<div align="center">

# 🚀 Happy Learning Linux 🐧

### Made for DevSecOps Linux Reference

</div>
