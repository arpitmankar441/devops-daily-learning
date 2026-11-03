# 05 – Amazon EBS

## What is EBS?

Amazon Elastic Block Store (EBS) provides block storage volumes for use with EC2 instances. EBS volumes persist independently of the running life of an instance, subject to their configuration and lifecycle settings.

## EBS volume types in the training notes

| Type | Description / use |
|---|---|
| General Purpose SSD (`gp3`, `gp2`) | General workloads, boot volumes, development and test |
| Provisioned IOPS SSD (`io1`, `io2`) | I/O-intensive workloads such as databases |
| Throughput Optimized HDD (`st1`) | Throughput-intensive workloads |
| Cold HDD (`sc1`) | Infrequently accessed workloads |
| Magnetic (`standard`) | Previous-generation magnetic volume type |

Check current AWS documentation for supported volume types and recommendations.

## Attach an EBS volume

1. Open the EC2 Console.
2. Select **Volumes**.
3. Choose the volume and select **Attach volume**.
4. Select the EC2 instance.
5. Attach the volume.

## Identify the attached device

Connect to the Linux instance and run:

```bash
lsblk
```

Device names shown inside Linux may differ from the name selected in the console. Identify the correct device carefully before formatting.

## Create a partition and filesystem

**Warning:** The following commands can destroy existing data if run against a device containing data. Confirm the correct empty volume first.

Example only, assuming the new device is `/dev/xvdf`:

```bash
sudo fdisk /dev/xvdf
```

In `fdisk`, use `n` to create a partition and `w` to write the changes.

Then create an ext4 filesystem on the new partition (example `/dev/xvdf1`):

```bash
sudo mkfs.ext4 /dev/xvdf1
```

## Mount the volume

```bash
sudo mkdir -p /mnt/ebs-volume
sudo mount /dev/xvdf1 /mnt/ebs-volume
df -h
```

## Persist the mount

For a persistent mount, use the filesystem UUID rather than relying on a device name.

```bash
sudo blkid
```

Add an appropriate UUID-based entry to `/etc/fstab`, then test carefully:

```bash
sudo mount -a
```

## EBS snapshots

A snapshot is a point-in-time backup of an EBS volume.

### Create a snapshot

1. Open EC2 → Volumes.
2. Select the volume.
3. Choose **Create snapshot**.
4. Add a description and create the snapshot.
5. Review it in the Snapshots section.

### Automate snapshots

Amazon Data Lifecycle Manager (DLM) can automate snapshot lifecycle policies. A policy can target tagged volumes and define a schedule and retention settings.

## Key takeaways

- EBS provides block storage for EC2.
- A volume can be attached, partitioned, formatted, and mounted.
- Snapshots can be used for backup and recovery.
- Check snapshot and storage costs.
