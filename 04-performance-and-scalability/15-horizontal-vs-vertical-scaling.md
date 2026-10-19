# 15. Horizontal vs Vertical Scaling

Scalability is a system's ability to handle more workload while meeting performance and reliability requirements.

## Vertical scaling

- Increase CPU, RAM, or storage resources on an existing machine.
- Often simpler initially.
- Has machine and service limits; a single machine can remain a failure point.

## Horizontal scaling

- Add more machines or application instances.
- Can increase capacity and resilience when designed correctly.
- Requires attention to distributed state, network failures, coordination, and shared dependencies.

## Comparison and example

- A small dashboard may work well on one larger server.
- A global commerce system may need multiple app instances, caching, replicas, and data partitioning.
- Choose based on cost, workload, performance, availability, and operational complexity.

> **Interview:** Horizontal scaling is not always better; it can improve capacity but introduces distributed-system complexity.
