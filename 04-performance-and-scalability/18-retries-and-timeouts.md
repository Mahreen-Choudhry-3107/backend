# 18. Retries & Timeouts

Timeouts bound how long an operation can wait. Retries repeat an operation after failures that may be temporary.

## Timeout examples

- Connection timeout.
- HTTP request timeout.
- Database command timeout.
- Upstream dependency timeout.

## Retry strategy

- Retry only failures likely to be transient.
- Bound the number of attempts.
- Use exponential backoff and random jitter.
- Respect service guidance and avoid retrying indefinitely.
- Use idempotency protection for operations that must not create duplicate effects.

## Circuit breaker

- Temporarily blocks calls to a dependency after a failure threshold.
- May allow limited trial requests later to check whether the dependency recovered.
- Can help prevent repeated calls from overwhelming a failing service.

> **Interview:** Retries can worsen an outage by increasing load. Bounded retries, backoff, jitter, timeouts, and circuit breakers help control the failure.
