# 08. Database Indexing

An index is a data structure that helps a database locate rows without scanning the entire table for every query.

## Example

- Query: `SELECT * FROM users WHERE email = 'zaid@example.com';`
- A useful index can make the lookup more efficient.
- Example: `CREATE INDEX idx_users_email ON users(email);`

## Common types

- **B-tree:** common for equality, range, and ordered access.
- **Composite:** indexes multiple columns; column order matters.
- **Unique:** enforces uniqueness for indexed key values.
- **Full-text:** supports text-search workloads in systems that provide it.

## Trade-offs and practices

- Indexes use storage and add overhead to inserts, updates, and deletes.
- Index frequently filtered or joined columns when measurements support it.
- Inspect query plans and data distribution.
- Avoid blindly indexing every column.
- The optimizer may choose a table scan when it estimates that to be cheaper.

> **Interview:** Indexes can speed up reads but slow writes because the database must maintain index structures when data changes.
