# 08 – Amazon VPC

## 1. What is a VPC?

Amazon Virtual Private Cloud (VPC) lets you launch AWS resources in a logically isolated virtual network that you define.

You control networking settings such as:

- IP address ranges
- Subnets
- Route tables
- Internet gateways
- Network ACLs
- Security groups

## 2. Key VPC components

### VPC

A logically isolated network in an AWS Region.

### Subnet

A range of IP addresses in a VPC. Each subnet belongs to one Availability Zone.

### Route table

Contains rules that determine where network traffic is directed.

### Internet Gateway (IGW)

Allows communication between a VPC and the internet when routes and other required settings are configured.

### Security Group

A stateful virtual firewall associated with supported resources.

### Network ACL

A subnet-level network control that is stateless.

### NAT Gateway

Allows resources in private subnets to initiate supported outbound internet connections without allowing unsolicited inbound internet connections.

## 3. Default VPC and custom VPC

- **Default VPC:** AWS can provide a default VPC in a Region, with default networking resources.
- **Custom VPC:** Created and configured to meet a specific network design.

## 4. AWS-reserved IPv4 addresses in each subnet

AWS reserves the first four IPv4 addresses and the last IPv4 address in each subnet CIDR block.

For example, in `192.168.1.0/24`, AWS reserves:

- `192.168.1.0` – network address
- `192.168.1.1` – VPC router
- `192.168.1.2` – DNS mapping
- `192.168.1.3` – reserved for future use
- `192.168.1.255` – reserved

## 5. CIDR calculation

For an IPv4 CIDR block:

```text
Total IP addresses = 2^(32 - prefix length)
```

Example:

```text
10.0.0.0/16
```

A `/16` contains 65,536 IPv4 addresses.

To divide `10.0.0.0/16` into four equal subnets, use `/18`:

- `10.0.0.0/18`
- `10.0.64.0/18`
- `10.0.128.0/18`
- `10.0.192.0/18`

Each `/18` contains 16,384 addresses.

## 6. Practical VPC exercise

Create a custom VPC in a test account:

1. Choose a non-overlapping IPv4 CIDR range, for example `10.0.0.0/16`.
2. Create one public subnet and one private subnet in separate or selected AZs.
3. Create and attach an Internet Gateway.
4. Create a public route table and add a default route to the Internet Gateway.
5. Associate the public subnet with that route table.
6. Configure private-subnet routing according to the exercise requirements.
7. Review security groups and network ACLs.
8. Launch test resources only after reviewing connectivity and cost.

## Key takeaways

- A VPC is regional.
- A subnet belongs to one AZ.
- Route tables control traffic paths.
- Security groups and network ACLs provide different layers of network control.
