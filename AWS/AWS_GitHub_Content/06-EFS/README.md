# 06 – Amazon EFS and NFS

## 1. What is NFS?

NFS means **Network File System**. It allows computers to share files over a network.

Two main parts:

- **NFS server:** Hosts the shared storage.
- **NFS clients:** Connect to and access the shared files.

A client mounts the shared directory and accesses it like a local directory.

### Key features

- Centralised storage
- Shared access
- Multiple clients can access shared data
- Files appear as a mounted directory
- NFS commonly uses TCP port 2049

## 2. NFS and Amazon EFS

Amazon Elastic File System (EFS) is a managed file storage service that supports the NFS protocol.

- An EFS file system is created in an AWS Region.
- Regional EFS storage can be accessed from multiple Availability Zones in that Region using mount targets and network connectivity.
- Security groups must allow NFS traffic on TCP port 2049 from the clients that need access.

## 3. Create an EFS file system

1. Open Amazon EFS in the AWS Console.
2. Choose **Create file system**.
3. Select the VPC.
4. Configure mount targets in the required Availability Zones/subnets.
5. Configure security groups to allow NFS TCP 2049 from the EC2 client security group.
6. Review performance and throughput settings.
7. Enable encryption at rest where appropriate.
8. Create the file system.

## 4. Install NFS utilities on Ubuntu / Debian

```bash
sudo apt-get update
sudo apt-get install -y nfs-common
```

## 5. Install EFS utilities on Amazon Linux

```bash
sudo yum install -y amazon-efs-utils
```

Depending on the operating system and chosen mount method, NFS client packages may also be required.

## 6. Mount EFS using NFSv4.1

Replace the file-system ID and Region with your actual values.

```bash
sudo mkdir -p /mnt/efs
sudo mount -t nfs4 -o nfsvers=4.1 FILE_SYSTEM_ID.efs.REGION.amazonaws.com:/ /mnt/efs
```

Example hostname format:

```text
fs-12345678.efs.us-east-1.amazonaws.com
```

## 7. Verify the mount

```bash
df -h
mount | grep efs
```

## 8. Troubleshooting checklist

- Confirm the EFS file system is available.
- Confirm a mount target exists in a reachable AZ.
- Confirm EC2 and EFS are in a network configuration that can communicate.
- Confirm the EFS mount-target security group allows inbound TCP 2049 from the EC2 security group.
- Confirm NFS client utilities are installed.
- Confirm the file-system ID and Region in the DNS name are correct.

## Practical task

Create an EFS file system, mount it on one Ubuntu EC2 instance, create a test file, and verify that the file is visible from a second authorised EC2 instance.
