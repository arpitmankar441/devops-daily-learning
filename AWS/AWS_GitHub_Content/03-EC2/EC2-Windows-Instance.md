# EC2 – Launch a Windows Instance

## Objective

Launch a Windows Server EC2 instance and connect using Remote Desktop Protocol (RDP).

## Launch steps

1. Sign in to the AWS Management Console.
2. Open EC2 and select the required Region.
3. Choose **Launch instance**.
4. Enter an instance name.
5. Select a Windows Server AMI.
6. Choose an instance type after checking its cost.
7. Configure storage and networking.
8. Create or select a key pair as required by the AMI and console workflow.
9. Configure the security group to allow RDP (TCP port 3389) only from your IP address.
10. Review and launch the instance.

## Retrieve the Windows administrator password

1. Select the running Windows instance in the EC2 Console.
2. Choose **Connect** or the password retrieval option.
3. Use the private key associated with the instance to decrypt the password, when required.
4. Copy the Administrator password securely.

## Connect using Remote Desktop

1. Open Remote Desktop Connection on Windows.
2. Enter the instance's public IPv4 address or DNS name.
3. Use the username `Administrator`.
4. Enter the retrieved password.

## Troubleshooting checklist

- Confirm that the instance is running and passed status checks.
- Confirm that it has a reachable public address or an appropriate private connection path.
- Confirm that the security group allows TCP 3389 from your current IP.
- Check that the correct Administrator password is being used.

## Security reminder

Do not expose RDP to the entire internet (`0.0.0.0/0`). Restrict access to a trusted IP range or use a more secure management option.
