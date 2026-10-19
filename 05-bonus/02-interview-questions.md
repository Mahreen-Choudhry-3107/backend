# Bonus 2. 15 Important Backend Interview Questions

### 1. What happens when you enter a URL in a browser?
Discuss DNS, connection establishment, TLS, HTTP requests, server processing, and browser rendering.

### 2. What is the difference between REST and GraphQL?
REST commonly exposes resources through endpoints; GraphQL lets clients request specific fields through a schema-based query language.

### 3. What is the difference between PUT and PATCH?
PUT generally replaces a resource representation; PATCH applies partial modifications.

### 4. Authentication vs authorization?
Authentication verifies identity; authorization checks permissions.

### 5. JWT vs sessions — which would you choose?
Discuss state management, revocation, scaling, storage, and browser security.

### 6. SQL vs NoSQL — when would you use each?
Discuss relationships, consistency, access patterns, query needs, and scaling requirements.

### 7. How does an index improve performance?
It can reduce data examined for supported queries, at the cost of storage and write overhead.

### 8. Explain ACID.
Atomicity, Consistency, Isolation, and Durability.

### 9. What is the N+1 query problem?
One query retrieves a collection, followed by one additional query per item.

### 10. Caching vs indexing?
Caching reuses stored values or results; indexing helps locate data efficiently in a data store.

### 11. How would you scale an API handling millions of requests?
Discuss profiling, caching, load balancing, stateless instances, database optimization, asynchronous work, and monitoring.

### 12. Why use message queues?
To decouple producers and consumers, buffer work, and process suitable tasks asynchronously.

### 13. How do you prevent SQL injection?
Use parameterized queries, safe database APIs, least-privilege access, and appropriate validation.

### 14. How would you handle a downstream service outage?
Discuss timeouts, bounded retries, exponential backoff, jitter, circuit breakers, safe fallbacks, and observability.

### 15. How would you prevent duplicate payment requests?
Use idempotency keys, persist operation state, enforce suitable uniqueness constraints, and understand the provider's guarantees.
