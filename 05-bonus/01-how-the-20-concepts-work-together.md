# Bonus 1. How the 20 Concepts Work Together

Example: a user purchasing a product from an e-commerce application.

## 1. Request
Frontend sends an HTTP request to a REST API over HTTPS.
**Concepts:** client–server architecture, REST, HTTP methods, TLS.

## 2. Authentication
Backend verifies identity and permissions.
**Concepts:** authentication, authorization, JWT or sessions.

## 3. Data retrieval
Backend reads product and inventory data.
**Concepts:** SQL/NoSQL, indexing, normalization, connection pooling.

## 4. Performance
Cache serves frequently accessed product information; queries are optimized to avoid unnecessary round trips.
**Concepts:** caching, N+1.

## 5. Order creation
Backend validates inventory and records the order transactionally.
**Concept:** transactions and ACID.

## 6. Traffic management
A load balancer routes requests across healthy instances.
**Concepts:** load balancing and horizontal scaling.

## 7. Background work
A queue processes confirmation emails and analytics asynchronously.
**Concept:** message queues.

## 8. Protection
Rate limiting controls excessive traffic and parameterized queries protect database access.
**Concepts:** rate limiting and SQL injection prevention.

## 9. Failure handling
Timeouts, bounded retries, and idempotency help prevent duplicate effects.
**Concept:** retries and timeouts.

## 10. Compatibility
API versioning supports older clients while the backend evolves.
**Concept:** API versioning.

> **Key takeaway:** backend engineering means building systems that are secure, reliable, maintainable, and capable of handling real-world traffic.
