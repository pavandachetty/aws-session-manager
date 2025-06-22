Here's a CloudFormation template that sets up an EC2 instance with AWS Systems Manager Session Manager enabled. It includes:

A VPC, Subnet, Security Group

An IAM Role with AmazonSSMManagedInstanceCore policy

An EC2 instance with the SSM Agent pre-installed (Amazon Linux 2 AMI)
