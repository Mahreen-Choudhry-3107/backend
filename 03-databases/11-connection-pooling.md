# 11. Connection Pooling

Connection pooling reuses database connections instead of opening a new connection for every request.

## How it works

- Application requests a connection from the pool.
- The pool provides an available connection.
- The application executes database operations.
- The connection is returned to the pool for reuse.

## Benefits

- Reduces connection-establishment overhead.
- Can improve throughput under suitable workloads.
- Limits concurrent connections and helps manage database resources.

## Configuration and mistakes

- Maximum pool size limits connections in a pool.
- Timeouts control how long acquisition or connection attempts wait, depending on the driver.
- Avoid oversized pools that overwhelm the database.
- Dispose of connections properly and do not hold them during unrelated slow work.
- Many application instances can collectively create too many connections.

> **Interview:** Pooling does not mean every connection stays open forever; the pool manages reusable connections according to its configuration and workload.
