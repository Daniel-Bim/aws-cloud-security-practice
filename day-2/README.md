# Day 2 – EC2 Instances: Public & Private + Network Connectivity

## 🧠 Objectives
- Practice EC2 instance creation in both public and private subnets.
- Test internet access and connectivity.
- Understand security implications of private vs. public resources.

## ✅ Actions Performed

### 🌐 Networking Setup
- Verified VPC, subnets, and route tables are correctly defined:
  - Public subnet has a route to an Internet Gateway.
  - Private subnet has no direct internet route.

### 🖥️ EC2 Public Instance
- Created a public EC2 instance.
- Successfully connected using **EC2 Instance Connect**.
- Verified internet connectivity using:
  - `ping 8.8.8.8`
  - `curl -I http://www.google.com`

### 🔒 EC2 Private Instance
- Created a private EC2 instance.
- Attempted SSH access via public instance (jump host logic).
  - Connection failed due to missing SSH keys and blocked access (expected behavior).
- Confirmed that private instances are not directly accessible from the internet.

## 📌 Key Learnings
- A public EC2 instance requires:
  - Subnet with a route to an Internet Gateway.
  - Auto-assigned public IP.
- Private EC2 instances must be accessed through:
  - Bastion hosts (jump servers), or
  - AWS Systems Manager Session Manager.

## 📂 Files Created
- `private-ec2-test.pem` – private key for SSH (not committed to repo).
- Updated documentation in `day-2/`.

## 🗂️ Status
✅ Networking and connectivity verified  
⚠️ SSH to private instance pending future Session Manager configuration

---

**Next:** Set up Session Manager or Bastion Host for private EC2 access.