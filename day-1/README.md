# Day 1 – IAM & VPC Setup (Security Foundations + Networking)

## 🎯 Objectives
- Create IAM user with restricted access
- Create a VPC with public and private subnets
- Attach Internet Gateway to enable internet access for public subnet

## 🔧 Steps Performed

### IAM (from prior session)
1. Created an IAM user with limited access to S3  
2. Created a custom IAM policy to block all except specific actions and restrict access to a specific bucket  
3. Attached the policy to the IAM user  

> ℹ️ Note: IAM setup was not performed in this specific session, but documented here as part of the overall foundation.

### VPC Setup
1. Created a VPC with CIDR block `192.168.0.0/16` in region `eu-central-1`  
2. Created a public subnet in `eu-central-1a` with CIDR `192.168.1.0/24`  
3. Created a private subnet in `eu-central-1b` with CIDR `192.168.2.0/24`  
4. Created an Internet Gateway named `MyIGW`  
5. Attached the Internet Gateway to the VPC and verified the attachment is `available`

## 📁 Files
- `iam-policy.json` – custom IAM policy attached to the user  

## 💡 Notes
- IAM policies should follow least privilege  
- CloudTrail was **not** set up yet (planned for future session)  
- Public subnet still needs a Route Table with route to the Internet Gateway  
- Next: configure Route Tables and test connectivity for both subnets
