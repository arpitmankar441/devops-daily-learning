# AWS – Student Assignments

Complete these exercises in a training account. Check pricing before creating resources and clean up when finished.

## Assignment 1 – Cloud Computing

1. Define virtualization.
2. Explain the role of a hypervisor.
3. Compare virtualization and cloud computing.
4. Explain IaaS, PaaS, and SaaS with examples.

## Assignment 2 – AWS Global Infrastructure

1. What is an AWS Region?
2. What is an Availability Zone?
3. Explain why a workload may be deployed across multiple AZs.
4. Find the Region selected in your AWS Console.

## Assignment 3 – EC2

1. What is EC2?
2. What is an AMI?
3. What is an instance type?
4. Explain the purpose of an EC2 key pair.
5. Launch a Linux test instance and connect using SSH.
6. Launch a Windows test instance only if your training budget permits, then connect using RDP.

## Assignment 4 – Security Groups

1. Explain inbound and outbound rules.
2. What is the default port for SSH?
3. What is the default port for RDP?
4. Create a security group allowing SSH from your IP.
5. Explain why SSH and RDP should not be exposed to everyone.

## Assignment 5 – EBS

1. What is EBS?
2. Explain the purpose of an EBS snapshot.
3. Attach a new empty EBS volume to a test instance.
4. Identify the volume using `lsblk`.
5. Create a filesystem and mount it.
6. Explain how to make a mount persistent.

## Assignment 6 – EFS

1. What is NFS?
2. What is Amazon EFS?
3. Which port is commonly used by NFS?
4. Create an EFS file system.
5. Mount it on an authorised EC2 instance.
6. Verify the mount using `df -h`.

## Assignment 7 – Networking

1. Define IP address, subnet mask, gateway, and DNS.
2. What is CIDR?
3. Calculate the total addresses in `/24`, `/20`, and `/16`.
4. Convert `/24` to dotted-decimal subnet mask.
5. Run `ip addr`, `ip route`, `ping`, and `nslookup`.

## Assignment 8 – VPC

1. What is a VPC?
2. What is a subnet?
3. Explain the purpose of an Internet Gateway.
4. Compare Security Groups and Network ACLs.
5. Create a VPC with one public subnet and one private subnet.
6. Explain the route table associated with each subnet.

## Final mini-project – Host a web page on EC2

1. Launch an Ubuntu EC2 instance.
2. Allow SSH from your IP and HTTP for the intended test audience.
3. Connect using SSH.
4. Install NGINX.
5. Create a simple HTML page.
6. Open the page using the instance's public address.
7. Record the steps and screenshots.
8. Stop or terminate resources and remove resources you no longer need.

## Submission format

For each assignment, submit:

- Objective
- AWS services used
- Steps performed
- Commands used
- Screenshots or command output
- Result
- Troubleshooting notes
