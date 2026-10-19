# 12. The N+1 Query Problem

The N+1 problem occurs when an application fetches a collection with one query, then issues another query for each item.

## Example

- One query fetches 100 orders.
- A separate query fetches the customer for each order.
- The total can be approximately 101 queries.

## Why it hurts

- More network round trips and latency.
- Increased database load.
- Performance degrades as collection size grows.

## Solutions

- Use a `JOIN` when a combined result is appropriate.
- Use ORM eager loading or batch fetching where suitable.
- Batch repeated lookups with DataLoader-style approaches in appropriate systems.
- Inspect SQL logs, query counts, and execution plans.
- Avoid joining multiple large one-to-many relationships blindly, as row counts can multiply.

> **Interview:** Debug by measuring query counts and timings, identifying repeated lookups, then comparing joins, batching, and eager-loading strategies.
