# 17. Rate Limiting

Rate limiting restricts how frequently a client or identity can make requests within a defined policy.

## Example

- An API might allow 100 requests per minute per authenticated user.
- When the limit is exceeded, return `429 Too Many Requests`.
- A `Retry-After` header may communicate when to retry.

## Common algorithms

- **Fixed window:** counts requests in fixed intervals; simple but can allow boundary spikes.
- **Sliding-window log:** tracks timestamps in a rolling window; accurate but potentially expensive.
- **Sliding-window counter:** approximates a rolling window using adjacent interval counters.
- **Token bucket:** requests consume tokens; supports controlled bursts.
- **Leaky bucket:** controls the rate at which requests are processed, depending on implementation.

## Where and how

- Apply at an API gateway, proxy, middleware, or endpoint.
- Use different policies for login, expensive operations, and general reads.
- Distributed applications may need shared counters or atomic operations.
- IP-only policies can affect users behind shared networks.
- Monitor rejected requests and tune limits based on real traffic.

> **Interview:** A distributed rate limiter can use an API gateway or shared store such as Redis with atomic counter operations or a suitable script.
