# Terraform - AWS SSM Session Manager Demo

This repository contains two separate Terraform configurations to demonstrate how to connect to EC2 instances using AWS Systems Manager Session Manager:

---

## 📁 Folders

### `public-ssm/`
- Provisions an EC2 instance in a **public subnet**.
- Uses **internet access** to communicate with the SSM service.
- Suitable for development/testing or where internet access is acceptable.

### `private-ssm/`
- Provisions an EC2 instance in a **private subnet**.
- Uses **VPC Endpoints** to securely connect to Systems Manager **without any internet access**.
- Ideal for production or isolated environments.

---

## 🛠 Usage

```bash
cd public-ssm   # or private-ssm
terraform init
terraform apply
```

## 🔐 Session Manager Access

Once deployed, start a session using:

```bash
aws ssm start-session --target <instance-id>
```

Make sure your local IAM user or role has permission: `ssm:StartSession`

---

## ✅ Prerequisites

- AWS CLI and credentials configured
- Terraform v1.0+
- An IAM user/role with admin privileges (or fine-tuned permissions for VPC, EC2, IAM, and SSM)

---

## 📌 Notes

- The Amazon Linux 2 AMI is used for EC2 instances.
- SSM agent is pre-installed in the AMI.
- You do **not need SSH or key pairs** to access instances.

---

