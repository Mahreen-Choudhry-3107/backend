# 14. Load Balancing

A load balancer distributes incoming requests across multiple server instances to reduce bottlenecks and support availability.

## Common algorithms

- **Round robin:** send requests in sequence across eligible servers.
- **Weighted round robin:** assign more traffic to servers with higher weights.
- **Least connections:** prefer fewer active connections, depending on implementation.
- **IP hash:** select a backend based on client IP information.

## Health checks and benefits

- Health checks help remove unhealthy instances from rotation.
- Traffic can be distributed across instances.
- Rolling maintenance and deployments can be supported with sufficient healthy capacity.
- Redundancy can improve availability.

## Design considerations

- Avoid relying on a single server for session state.
- Use meaningful readiness checks.
- Database and other dependencies must also have enough capacity.
- A load balancer itself may need redundancy.
- Retries can amplify overload if poorly configured.

> **Interview:** When an instance fails health checks, the load balancer can stop routing new requests to it, assuming other instances have sufficient capacity.
