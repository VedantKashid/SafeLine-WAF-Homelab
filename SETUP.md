# Quick Setup Guide

## Prerequisites
- VMware Workstation installed
- Ubuntu 24.04 LTS ISO
- Kali Linux 2025.1 ISO
- Minimum 8GB RAM available

## Quick Start Commands

### Ubuntu Server Setup
```bash
# One-liner LAMP installation
sudo apt update && sudo apt install -y apache2 mariadb-server php php-mysqli php-gd libapache2-mod-php git curl

# Clone DVWA
cd /var/www/html && sudo git clone https://github.com/digininja/DVWA.git

# Install SafeLine WAF
sudo bash -c "$(curl -fsSLk https://waf.chaitin.com/release/latest/manager.sh)" -- --en
```

### Kali Linux Setup
```bash
# Update /etc/hosts
echo "10.227.251.226 webserver.lab" | sudo tee -a /etc/hosts

# Test connectivity
curl -k https://webserver.lab/
```

## Default Credentials

| Service | Username | Password |
|---------|----------|----------|
| DVWA | admin | password |
| MariaDB | dvwa_user | p@ssw0rd123 |
| SafeLine WAF | (generated during install) | (check installation output) |
