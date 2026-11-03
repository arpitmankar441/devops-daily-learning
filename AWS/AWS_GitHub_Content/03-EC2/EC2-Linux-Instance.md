# EC2 – Launch a Linux Instance

## Objective

Launch an Ubuntu EC2 instance and prepare it for SSH access.

## Steps in the AWS Console

1. Sign in to the AWS Management Console.
2. Select the required Region.
3. Search for **EC2** and open the service.
4. Choose **Launch instance**.
5. Enter an instance name, for example `MyFirstInstance`.
6. Select an Ubuntu Server AMI.
7. Select an instance type appropriate for the exercise and budget.
8. Configure the network settings.
9. Create or select a key pair.
10. Configure the security group to allow SSH (TCP port 22) from **My IP**.
11. Review the storage configuration.
12. Review the estimated charges and launch the instance.

## Connect from Linux, macOS, or Windows PowerShell

First, locate the downloaded private key file and the instance's public IPv4 address.

```bash
chmod 400 /path/to/key.pem
ssh -i /path/to/key.pem ubuntu@PUBLIC_IP_ADDRESS
```

Replace `/path/to/key.pem` and `PUBLIC_IP_ADDRESS` with your actual values.

The default username for many Ubuntu EC2 AMIs is `ubuntu`. The username can differ for other AMIs.

## Verify the connection

After connecting, run:

```bash
whoami
hostname
uptime
ip addr
df -h
```

## Security reminders

- Restrict SSH access to your own public IP address where possible.
- Never share or upload your private key.
- Do not leave unused instances running.
- Check current pricing and Free Tier eligibility; instance eligibility varies by account, Region, and offer.
