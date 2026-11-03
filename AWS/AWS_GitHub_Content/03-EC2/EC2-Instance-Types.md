# EC2 – Instance Types

EC2 offers different instance families for different workload requirements.

| Category | Purpose | Examples from training notes |
|---|---|---|
| General purpose | Balanced compute, memory, and networking | M5, T2, T3, M6a |
| Compute optimized | Compute-intensive workloads | C5, C6i, C7g |
| Memory optimized | Memory-intensive workloads and databases | R5, X1, X2idn |
| Storage optimized | High local storage performance | I3, D2, H1 |
| Accelerated computing | GPU or specialised accelerator workloads | P3, G5, Inf1 |
| High-performance computing | HPC workloads | Hpc6a, Hpc7g |

**Note:** Instance families and available sizes change. Check the current EC2 instance type documentation and Region availability before selecting an instance.

## How to choose an instance type

Consider:

1. CPU requirements
2. Memory requirements
3. Storage requirements
4. Network performance
5. Operating system and software compatibility
6. Cost

## Student exercise

For each scenario, identify which instance category is a sensible starting point:

- A general web application
- A CPU-intensive batch job
- An in-memory database
- A workload requiring GPU acceleration
