# aws-networking
## Overview
This project involves setting up a Virtual Private Cloud (VPC) with public and private subnets, configuring a NAT Gateway, implementing security groups and network ACLs, and testing SSH access between instances.
## Steps Taken
1. Created a Virtual Private Cloud (VPC) with Subnets

	•	Created a VPC with CIDR 10.0.0.0/16.

	•	Created a public subnet (10.0.1.0/24) in us-east-1a.

	•	Created a private subnet (10.0.2.0/24) in us-east-1b.

	•	Enabled auto-assign public IP for the public subnet.

2. Set Up an Internet Gateway (IGW)

	•	Created and attached an Internet Gateway (IGW) to the VPC.

	•	Updated the public route table to route 0.0.0.0/0 traffic through the IGW.

3. Created a NAT Gateway for Private Subnet

	•	Allocated an Elastic IP (EIP).

	•	Created a NAT Gateway in the public subnet.

	•	Updated the private route table to send outbound traffic (0.0.0.0/0) through the NAT Gateway.

4. Created and Launch EC2 Instances

	•	Created a key pair for SSH access.

	•	Launched a Public EC2 instance in the public subnet (Amazon Linux).

	•	Launched a Private EC2 instance in the private subnet (Amazon Linux).

	•	Assigned the respective security groups.

5. SSH into the Public EC2 Instance

	•	Used Git Bash to SSH into the public instance:

ssh -i "m4ace-new-key-pair.pem" ec2-user@<public-ip>

6. Created Network ACLs (NACLs)

7. created security group

# Challenges encountered
Despite several attempts, I could not access the private instance EC2 via the public.
