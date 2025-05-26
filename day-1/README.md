# Day 1 – IAM, CloudTrail & VPC Setup (Security Foundations + Networking)

## 🎯 Objectives
- Set up secure IAM policies using least privilege
- Enable CloudTrail for activity logging
- Create a VPC with public and private subnets
- Attach Internet Gateway to enable internet access for public subnet

## 🔧 Steps Performed

### IAM & CloudTrail
1. Created IAM user with limited access to S3  
2. Created custom IAM policy to block all except specific actions and restrict access to a specific bucket  
3. Attached policy to the IAM user  
4. Enabled CloudTrail in the region  
5. Simulated a security-related action (e.g., failed access) and verified it was logged  

### VPC Setup
1. Created a VPC with CIDR block `192.168.0.0/16` in `eu-central-1` region  
2. Created a public subnet in `eu-central-1a` with CIDR `192.168.1.0/24`  
3. Created a private subnet in `eu-central-1b` with CIDR `192.168.2.0/24`  
4. Created an Internet Gateway named `MyIGW`  
5. Attached the Internet Gateway to the VPC and verified the attachment is `available`

## 📁 Files
- `iam-policy.json` – custom IAM policy attached to the user  
- `cloudtrail-sample-log.json` – example log from CloudTrail  

## 💡 Notes
- Always follow least privilege principle with IAM policies  
- Enable CloudTrail across all regions for comprehensive monitoring  
- Public subnet requires a route table that directs traffic to the Internet Gateway  
- Next steps: configure Route Tables and test connectivity for public and private subnets

