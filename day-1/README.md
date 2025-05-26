# Day 1 – IAM & CloudTrail Setup (Security Foundations)

## 🎯 Objectives
- Set up secure IAM policies using least privilege
- Enable CloudTrail for activity logging
- Simulate and monitor a security-related action

## 🔧 Steps Performed
1. Created IAM user with limited access to S3
2. Created custom IAM policy:
   - Block all except specific actions
   - Restrict access to specific bucket
3. Attached policy to the user
4. Enabled CloudTrail in the region
5. Simulated action (e.g. failed access) and verified log

## 📁 Files
- `iam-policy.json` – policy attached to the IAM user
- `cloudtrail-sample-log.json` – sample log from CloudTrail

## 💡 Notes
- IAM policies should follow least privilege
- CloudTrail must be enabled across all regions for full coverage
- Next step: trigger alarm when unusual activity occurs
