# DevOps Log 🚀

A personal log of DevOps tools, labs, and Linux commands.

---

## 📁 1. File & Directory Management

```bash
pwd                    # Show current directory
ls -la                 # List all files with details
cd /path/to/dir        # Change directory
mkdir -p projects/lab  # Create nested folders
rm -rf folder/         # Delete folder
cp -r source/ dest/    # Copy files/folders
mv oldname newname     # Move or rename
touch file.txt         # Create empty file
```

---

## 🔍 2. File Search & Text Processing

```bash
find / -name "file.txt"        # Find file by name
grep -r "error" /var/log/      # Search text in files
sed -i 's/old/new/g' file.txt  # Find and replace
awk '{print $1}' file.txt      # Print first column
```

---

## 👤 3. User & Permission Management

```bash
whoami                     # Show current user
sudo su                    # Switch to root
chmod 755 file.sh          # Change permissions
chown user:group file.txt  # Change ownership
```

---

## 🌐 4. Networking

```bash
ip a                          # Show IP address
ping google.com               # Test connectivity
curl -I https://example.com   # Check HTTP response
ssh user@192.168.1.1          # Connect via SSH
netstat -tulnp                # Show open ports
```

---

## ⚙️ 5. System Services

```bash
systemctl start nginx     # Start service
systemctl stop nginx      # Stop service
systemctl restart nginx   # Restart service
systemctl status nginx    # Check status
systemctl enable nginx    # Auto-start on boot
journalctl -u nginx       # View service logs
```

---

## 💾 6. Disk & Memory

```bash
df -h                  # Disk space usage
du -sh folder/         # Folder size
free -h                # Memory usage
lsblk                  # List block devices
```

---

## 📋 7. Logs & Monitoring

```bash
tail -f /var/log/nginx/access.log  # Live log view
journalctl -f                       # Live system journal
journalctl --since "1 hour ago"    # Recent logs
uptime                              # System uptime
```

---

## 🐳 8. Docker Commands

```bash
docker ps                           # Running containers
docker ps -a                        # All containers
docker images                       # List images
docker build -t myapp .             # Build image
docker run -d -p 80:80 nginx        # Run container
docker stop container_id            # Stop container
docker logs container_id            # View logs
docker exec -it container bash      # Enter container
docker-compose up -d                # Start all services
docker-compose down                 # Stop all services
```

---

## 🔁 9. Git Commands

```bash
git clone https://github.com/...   # Clone repo
git status                          # Check changes
git add .                           # Stage all changes
git commit -m "message"             # Commit changes
git push origin main                # Push to GitHub
git pull origin main                # Pull latest
git branch                          # List branches
git checkout -b new-branch          # Create new branch
```

---

## 🔐 10. SSH & Security

```bash
ssh-keygen -t rsa           # Generate SSH key
ssh-copy-id user@server     # Copy key to server
ufw status                  # Firewall status
ufw allow 80/tcp            # Allow port 80
ufw enable                  # Enable firewall
```