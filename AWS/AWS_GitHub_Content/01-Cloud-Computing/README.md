# 01 – Introduction to Virtualization and Cloud Computing

## 1. Introduction to Virtualization

**Virtualization** is the creation of a virtual version of hardware, allowing multiple operating systems to run on a single physical machine.

### Types of virtualization

- **Server virtualization:** Multiple virtual servers run on one physical machine.
- **Storage virtualization:** Multiple physical storage devices are presented as a single virtual unit.
- **Network virtualization:** Network resources are abstracted into a manageable virtual framework.

### Benefits

- Efficient resource utilization
- Cost savings
- Scalability
- Simplified management

### How virtualization works

A **hypervisor** manages virtual machines (VMs). Examples include VMware, VirtualBox, KVM, Xen, and Microsoft Hyper-V.

**Example:** A company can run a legacy Windows application in a virtual machine hosted on a Linux server.

**Simple analogy:** A physical machine is like a house, and each VM is like a separate room with its own tenant (operating system).

## 2. Virtualization vs. Cloud Computing

Virtualization is a foundational technology. Cloud computing builds on technologies such as virtualization to deliver resources on demand.

| Feature | Virtualization | Cloud computing |
|---|---|---|
| Definition | Technology for creating virtual environments | Delivery of on-demand computing resources |
| Deployment | Often on-premises | Commonly delivered over the internet |
| Scalability | Limited by available physical capacity | Can scale using a provider's infrastructure |
| Access | Depends on the configured network | Commonly accessible over the internet |

**Analogy:** Virtualization is like owning apartments in a building; cloud computing is like renting accommodation when needed.

## 3. Cloud Service Models

### Infrastructure as a Service (IaaS)

Provides virtualized infrastructure such as compute, storage, and networking.

- Example: Amazon EC2, Google Compute Engine.
- Example use: Launch an EC2 virtual server and manage its operating system and applications.

### Platform as a Service (PaaS)

Provides a platform for developing and deploying applications without managing all the underlying infrastructure.

- Example: AWS Elastic Beanstalk, Google App Engine.
- Example use: Deploy an application using Elastic Beanstalk.

### Software as a Service (SaaS)

Provides software that users access over the internet.

- Examples: Gmail, Salesforce, Google Docs.

**Simple analogy:**
- IaaS: Rent an unfurnished apartment and manage it yourself.
- PaaS: Rent a furnished apartment and focus on your own setup.
- SaaS: Stay in a hotel where the service is ready to use.

## 4. Creating an AWS Account – Learning Checklist

The original training notes describe this general signup flow:

1. Visit the official AWS website and choose the account sign-up option.
2. Enter an email address, password, and account name.
3. Choose the appropriate account type.
4. Provide the requested payment details for verification.
5. Complete identity and phone verification.
6. Choose a support plan appropriate to your needs.
7. Sign in to the AWS Management Console.

**Important:** Signup requirements, Free Tier offers, payment verification, and support-plan choices can change. Follow the current instructions shown by AWS. Do not assume every service or usage level is free.

## Hands-on practice

1. Create or access an AWS account.
2. Sign in to the AWS Management Console.
3. Find EC2, S3, and RDS using the service search.
4. Identify the account menu and selected AWS Region.
5. Open the billing area and review the available cost-management tools.

## Key takeaways

- Virtualization allows multiple virtual environments to share physical hardware.
- Cloud computing delivers resources on demand.
- IaaS, PaaS, and SaaS describe different levels of managed services.
- Check current AWS pricing before creating resources.
