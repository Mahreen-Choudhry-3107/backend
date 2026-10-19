# Bonus 3. Practical Project — URL Shortener

Build a service that converts long URLs into short links and redirects users to the original destinations.

## Core features

- User registration and login.
- Create short URLs and redirect short links.
- Track click counts and view analytics.
- Rate-limit URL creation.
- Cache frequently accessed URL mappings.

## Suggested database tables

| Table | Fields |
|-------|--------|
| `USERS` | id, name, email, password_hash, created_at |
| `URLS` | id, user_id, short_code, original_url, created_at, expires_at |
| `URL_CLICKS` | id, url_id, clicked_at, referrer |

## Example API endpoints

```http
POST   /api/auth/register
POST   /api/auth/login
POST   /api/urls
GET    /api/urls/{shortCode}
GET    /api/urls/{shortCode}/analytics
DELETE /api/urls/{id}
```

## Concepts you will practice

- REST API design and HTTP status codes.
- Authentication, authorization, and database schema design.
- Indexing `short_code` and enforcing uniqueness constraints.
- Transactions, caching with Redis, and rate limiting.
- Input validation and safe URL handling.
- Connection pooling, API versioning, horizontal scaling, monitoring, and failure handling.

## Advanced challenges

1. Prevent duplicate short codes with a database uniqueness constraint.
2. Cache popular URL mappings.
3. Design a reliable click-tracking pipeline.
4. Use a queue for analytics processing.
5. Protect against malicious URLs and abuse.
6. Measure API latency and database query performance.
7. Explain how the service would handle millions of redirects.

> **Interview tip:** Be ready to explain why you chose each design, what trade-offs it introduces, and how you would measure whether it works.
