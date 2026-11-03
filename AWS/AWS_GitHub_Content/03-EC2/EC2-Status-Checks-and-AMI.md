# EC2 – Status Checks and AMIs

## 1. EC2 Status Checks

AWS performs status checks to help identify problems affecting an instance.

### System status check

Checks the AWS infrastructure supporting the instance.

### Instance status check

Checks the instance's operating system and network configuration.

### Common causes of problems

- Networking configuration issues
- Exhausted memory
- File-system problems
- Kernel or operating-system issues

CloudWatch alarms can monitor status-check metrics and, where supported and configured, trigger actions such as instance recovery.

## 2. AMI – Amazon Machine Image

An **Amazon Machine Image (AMI)** provides the information required to launch an EC2 instance, including the operating system and configured software.

### AMI storage types in the training notes

- **EBS-backed AMI:** The root volume is backed by Amazon EBS.
- **Instance-store-backed AMI:** The root volume is backed by instance store.

### Create an AMI

1. Open the EC2 Console.
2. Select the instance.
3. Choose **Actions → Image and templates → Create image** (console wording may change).
4. Enter an image name and description.
5. Review the settings and create the image.
6. Check the AMIs section for the resulting image.

### Copy an AMI

An AMI can be copied to another Region when supported. This can help with regional deployment and recovery planning.

## 3. Launch Templates

A launch template stores configuration used when launching EC2 instances.

It can include:

- AMI ID
- Instance type
- Key pair
- Security groups
- Storage and other launch settings

### Create a launch template

1. Open the EC2 Console.
2. Select **Launch Templates**.
3. Choose **Create launch template**.
4. Enter a template name.
5. Configure the AMI, instance type, key pair, and security group.
6. Review and create the template.

## Practical task

Create a test launch template without launching an instance. Identify which settings are saved in the template.
