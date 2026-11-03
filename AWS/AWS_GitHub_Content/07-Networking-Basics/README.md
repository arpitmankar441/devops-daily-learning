# 07 – Networking Basics

Networking connects devices so they can exchange data and share resources.

## 1. Important networking components

### IP address

An IP address identifies a device or network interface for communication.

- IPv4 example: `192.168.1.10`
- IPv6 example: `2001:db8::1`

### Subnet mask

A subnet mask identifies the network and host portions of an IPv4 address.

Example: `255.255.255.0` is the same prefix length as `/24`.

### Gateway

A gateway forwards traffic from one network to another.

### DNS

Domain Name System (DNS) translates domain names, such as `example.com`, into IP addresses.

### MAC address

A Media Access Control (MAC) address identifies a network interface at the data-link layer.

## 2. Types of networks

- **LAN:** Local Area Network, such as a home or office network.
- **WAN:** Wide Area Network, spanning larger geographic areas.
- **VLAN:** Virtual LAN, used to logically segment a network.

## 3. Common protocols

| Protocol | Purpose |
|---|---|
| TCP/IP | Core protocol suite for network communication |
| HTTP | Transfers web content |
| HTTPS | Encrypted web communication |
| FTP | File transfer protocol |
| SSH | Secure remote administration |

## 4. CIDR

CIDR means **Classless Inter-Domain Routing**. CIDR notation represents an IP network using an address and prefix length.

Example:

```text
192.168.1.0/24
```

`/24` means that 24 bits are used for the network prefix and 8 bits remain for host addresses.

### IPv4 address calculation

For a conventional IPv4 subnet:

- Total addresses = `2^(32 - prefix length)`
- Traditional usable host addresses = total addresses minus network and broadcast addresses.

Example for `/24`:

- Total addresses = `2^(32 - 24) = 256`
- Traditional usable host addresses = `256 - 2 = 254`

Special-purpose subnets and cloud networking rules can differ.

## 5. Subnetting example

Split `192.168.1.0/24` into four equal subnets by using `/26`:

- `192.168.1.0/26`
- `192.168.1.64/26`
- `192.168.1.128/26`
- `192.168.1.192/26`

## 6. Useful Linux commands

```bash
ip addr
ip route
ping 8.8.8.8
nslookup example.com
```

## Homework

1. Explain the difference between an IP address and a MAC address.
2. What is the purpose of a default gateway?
3. What does DNS do?
4. Calculate total IPv4 addresses in a `/24`.
5. Convert `/24` to a subnet mask.
6. Explain the difference between TCP and UDP.
