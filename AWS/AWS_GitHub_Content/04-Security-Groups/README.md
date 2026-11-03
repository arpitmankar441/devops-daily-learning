# 04 – Security Groups

## What is a Security Group?

A Security Group acts as a virtual firewall for supported AWS resources, such as EC2 instances. It controls inbound and outbound traffic.

## Inbound and outbound rules

- **Inbound rules:** Define traffic allowed to reach the resource.
- **Outbound rules:** Define traffic allowed to leave the resource.

Rules commonly specify a protocol, port range, and source or destination.

## Common ports

| Service | Protocol | Port | Purpose |
|---|---|---:|---|
| SSH | TCP | 22 | Remote access to Linux |
| HTTP | TCP | 80 | Web traffic |
| HTTPS | TCP | 443 | Encrypted web traffic |
| RDP | TCP | 3389 | Remote access to Windows |

## Create a Security Group

1. Open the EC2 Console.
2. Navigate to **Security Groups**.
3. Choose **Create security group**.
4. Enter a name and description.
5. Select the VPC.
6. Add only the required inbound rules.
7. Review outbound rules.
8. Create the security group.
9. Attach it to the instance.

## Example rules for a training web server

| Type | Port | Source |
|---|---:|---|
| SSH | 22 | My IP |
| HTTP | 80 | Only the audience needed for the demo |

For RDP, allow TCP 3389 only from a trusted IP range.

## Best practices

- Do not open SSH or RDP to everyone.
- Allow only required ports and sources.
- Use separate security groups for different application roles.
- Review rules regularly.

## Practical task

Create a security group that permits SSH from your IP and HTTP for a test website. Attach it to a test EC2 instance and verify access.
