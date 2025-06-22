
SSM with Private EC2 via VPC Endpoints (CloudFormation Template)

Here’s an enhanced CloudFormation template that sets up an EC2 instance in a private subnet, with no internet access, using AWS Systems Manager Session Manager via VPC Endpoints. 

This is ideal for secure, isolated environments (e.g., production or regulated workloads).

 Notes:
This instance has no internet access or NAT Gateway.

The SSM connection is routed via VPC endpoints (Interface type).

Ensure SSM Agent is running (pre-installed on Amazon Linux 2).

Replace t3.micro or modify tags/roles to suit your standards.