# EC2 – SSH Connection

## What is SSH?

SSH (Secure Shell) is a network protocol for securely accessing and managing remote systems over an encrypted connection.

## Key features

- Encrypted communication
- Key-based or password-based authentication, depending on configuration
- Remote command execution
- Secure file transfer using tools such as `scp` and `rsync`
- Port forwarding

## SSH in AWS EC2

For many Linux EC2 instances:

- Default SSH port: TCP 22
- Authentication commonly uses the EC2 key pair.
- The security group must allow inbound SSH from the connecting client.

## Connect to an instance

```bash
chmod 400 /path/to/key.pem
ssh -i /path/to/key.pem ubuntu@PUBLIC_IP_ADDRESS
```

Replace the key path and public IP with your own values.

## Common SSH client options

- Linux/macOS: Open a terminal and use `ssh`.
- Windows: Use PowerShell or Windows Terminal with the OpenSSH client. PuTTY is another option.

## Troubleshooting

1. Confirm the instance is running.
2. Confirm you are using the correct public IP or DNS name.
3. Confirm the security group allows TCP port 22 from your IP.
4. Confirm the route and network ACLs allow the connection.
5. Confirm the correct username for the selected AMI.
6. Confirm the private key matches the instance's key pair.
7. On Linux/macOS, check private-key permissions:

```bash
chmod 400 /path/to/key.pem
```

## Student practical

Connect to an Ubuntu EC2 instance using SSH. Run `whoami`, `hostname`, and `uptime`, then disconnect using `exit`.
