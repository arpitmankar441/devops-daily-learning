# 02 – AWS Global Infrastructure

## 1. AWS Management Console

The AWS Management Console is the web interface used to manage AWS resources.

You can use it to:

- Access services such as EC2, S3, RDS, and Lambda.
- Monitor usage and billing.
- Configure security settings and permissions.

### Main dashboard components

- **Navigation bar:** Shows account-related controls and the selected Region.
- **Service search:** Finds AWS services by name.
- **Resource groups:** Helps organise related resources.
- **Recently visited services:** Provides quick access to services used recently.
- **Build a solution:** Offers shortcuts to common tasks.

### Best practices

- Check the selected Region before creating resources.
- Review billing and usage regularly.
- Use resource names and tags that make ownership and purpose clear.

## 2. Region

An AWS **Region** is a separate geographic area where AWS operates infrastructure.

Examples include:

- Asia Pacific (Mumbai) – `ap-south-1`
- US East (N. Virginia) – `us-east-1`

Choose a Region based on factors such as user location, latency, service availability, compliance requirements, and cost.

## 3. Availability Zone (AZ)

An **Availability Zone** is an isolated location within an AWS Region. A Region contains multiple Availability Zones, connected through AWS's network.

### Why Regions and AZs matter

- **High availability:** Deploying across multiple AZs can reduce the impact of an AZ-level failure.
- **Low latency:** Selecting a Region closer to users can reduce network latency.
- **Resilience:** Separate AZs help design fault-tolerant applications.

### Example

The Mumbai Region has Availability Zones identified by names such as `ap-south-1a`, `ap-south-1b`, and `ap-south-1c`. The exact AZ mapping can vary between AWS accounts.

## Quick comparison

| Region | Availability Zone |
|---|---|
| Geographic area | Isolated location within a Region |
| Contains multiple AZs | Belongs to one Region |
| Example: `ap-south-1` | Example: `ap-south-1a` |

## Practical task

1. Sign in to the AWS Console.
2. Find the Region selector.
3. Identify the Region currently selected.
4. Open EC2 and observe the AZ choices when viewing or creating an instance.
5. Explain why a production application might use more than one AZ.
