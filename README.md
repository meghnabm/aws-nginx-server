# AWS Nginx Web Server Project

## Project Overview

This project demonstrates deployment of an Nginx web server on AWS EC2 while covering key AWS Solutions Architect Associate concepts.

---

## AWS Services Used

- IAM
- EC2
- Security Groups
- EBS
- AMI

---

## Architecture
```
Internet
↓
Security Group
↓
EC2 Instance
↓
Nginx Web Server
↓
EBS Volume
```
---

## Implementation Steps

### 1. IAM Setup

- Created IAM Group: Admins
- Attached AdministratorAccess policy
- Created IAM User: meghna-admin
- Added user to Admins group

---

### 2. EC2 Deployment

- Launched Ubuntu EC2 instance
- Generated Key Pair
- Configured Security Group

Ports Allowed:

- 22 (SSH)
- 80 (HTTP)

---

### 3. Nginx Installation

Installed Nginx and verified access using public IP.

```bash
sudo apt update
sudo apt install nginx -y
```

---

### 4. Additional Storage

Created and attached EBS Volume.

```bash
lsblk
sudo mkfs.ext4 /dev/nvme1n1
sudo mount /dev/nvme1n1 /data
```

---

### 5. AMI Creation

Created custom AMI for future server deployment.

---

## Screenshots

### IAM User

screenshots/IAM-user-creation.png
screenshots/IAM-set-perm.png
screenshots/IAM-user-created.png

### EC2 Instance

screenshots/instance-created.png

### Nginx Running

screenshots/nginx_running.png
screenshots/custom-page.png

### EBS Mounted

screenshots/ebs-mounted.png

### AMI Created

screenshots/ami-created.png

---

## Key Learnings

- IAM administration
- EC2 provisioning
- Security Groups
- Nginx deployment
- EBS management
- AMI creation

---

## AWS SAA Topics Covered

✅ IAM

✅ EC2

✅ Security Groups

✅ EBS

✅ AMI

✅ SSH

✅ Basic Networking
