# EC2 – Purchasing Options

AWS provides different EC2 purchasing options for different workload patterns.

## 1. On-Demand Instances

- Pay for compute capacity without a long-term commitment.
- Useful for short-term, variable, or unpredictable workloads.
- Pricing depends on the instance, operating system, Region, and usage.

## 2. Reserved Instances

- A one-year or three-year commitment for eligible EC2 usage.
- Can provide a discount compared with On-Demand pricing.
- Regional and zonal scope options have different characteristics.
- Convertible Reserved Instances allow certain configuration changes.

## 3. Spot Instances

- Use spare EC2 capacity at a potentially significant discount.
- AWS can interrupt Spot Instances when capacity is needed or market conditions require it.
- Suitable for interruption-tolerant workloads such as batch processing and distributed tasks.
- Generally unsuitable for workloads that cannot tolerate interruption.

## 4. Dedicated Hosts

- A physical server dedicated to your use.
- Can help meet certain software licensing and compliance requirements.
- Provides visibility and control over host placement.

## 5. Dedicated Instances

- EC2 instances running on hardware dedicated to a single customer.
- They do not provide the same host-level visibility and control as Dedicated Hosts.

## 6. Capacity Reservations

- Reserve On-Demand capacity in a specified Availability Zone.
- Can be created or cancelled according to the applicable rules.
- Capacity reservation itself does not automatically provide a pricing discount.

## 7. Savings Plans

Savings Plans offer lower prices in exchange for a commitment to a consistent amount of eligible usage over a one-year or three-year term.

## Simple analogy

- **On-Demand:** Pay when you use a room.
- **Reserved:** Make a longer commitment for a lower rate.
- **Spot:** Use spare capacity that may not always remain available.
- **Dedicated Host:** Reserve an entire physical building.
- **Capacity Reservation:** Reserve capacity even if you do not use it.

## Important

The original lecture notes contain historical pricing examples and discount percentages. These are not fixed guarantees. Always check current AWS pricing, commitment terms, and regional availability before making a purchasing decision.

## Student exercise

Choose a suitable purchasing option for:
1. A temporary test server.
2. A fault-tolerant batch-processing job.
3. A predictable workload running continuously.
4. A workload that must have capacity available in a particular AZ.
