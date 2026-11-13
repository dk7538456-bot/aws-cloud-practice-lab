# EC2 lab: launch a Linux instance

## Goal

Practice provisioning and connecting to a small Linux EC2 instance while keeping its network exposure limited.

## Console exercise

1. Pick a region and check the account's free-tier eligibility, current pricing, quotas, and available training sandbox rules.
2. Open EC2 and launch an eligible small Amazon Linux or Ubuntu instance. Use a descriptive lab name and the smallest suitable instance type.
3. Create or select a key pair and store the private key securely. Never commit it to this repository.
4. Configure the security group to allow SSH (TCP 22) only from your current public IP address. Do not open SSH to `0.0.0.0/0`.
5. Launch the instance and connect using the AWS Console's supported connection method or SSH from an authorized device.
6. Verify the operating system and instance metadata from the session. Do not install software or expose services beyond what the exercise needs.
7. Terminate the instance and remove its lab-only key pair and security group when finished.

## Optional AWS CLI inspection

With AWS CLI v2 already configured for the intended lab account, inspect the caller identity before making changes:

```sh
aws sts get-caller-identity
aws ec2 describe-instances --region YOUR_REGION
```

These commands are read-only. Do not paste credentials or account-specific output into a public issue.

