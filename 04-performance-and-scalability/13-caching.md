# 13. Caching

Caching stores frequently accessed data in a faster layer so the system can avoid repeating expensive work.

## Common cache types

- **Browser cache:** stores eligible resources in the browser.
- **CDN cache:** stores content at edge locations.
- **Application cache:** stores computed or frequently used values.
- **Distributed cache:** a shared system such as Redis or Memcached.
- Database systems may also cache internal data or selected results.

## Cache-aside pattern

- Check the cache first.
- On a hit, return the cached value.
- On a miss, query the source of truth.
- Store the result in cache, then return it.

## Common problems

- **Cache invalidation:** remove or refresh old values after source data changes.
- **Cache stampede:** many requests reload the same expired value simultaneously.
- **Stale data:** cache contains an outdated value.
- **Cache penetration:** repeated misses bypass the cache.

## Practices

- Choose appropriate TTLs.
- Invalidate or update entries when data changes.
- Consider negative caching, request coalescing, or locks for expensive misses.
- Protect sensitive data and monitor hit rate, latency, memory, and evictions.

> **Interview:** Caching improves suitable read workloads, but introduces freshness and invalidation trade-offs.
