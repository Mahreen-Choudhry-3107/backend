# 07. SQL vs NoSQL

SQL databases typically use relational tables and relationships. NoSQL is an umbrella term for several data models, including document, key-value, wide-column, and graph databases.

## SQL strengths

- Relational modeling and joins.
- Constraints and transaction support.
- Structured querying and reporting.
- Mature indexing and query optimization.

## NoSQL models and examples

- **Document:** MongoDB.
- **Key-value:** Redis.
- **Wide-column:** Cassandra.
- **Graph:** Neo4j.

## Choosing a model

- Use SQL when relational integrity, complex queries, and multi-record transactions are central.
- Consider NoSQL when its data model and distribution characteristics match the workload.
- SQL can scale horizontally; NoSQL is not automatically faster.
- Many systems combine relational storage with caches or specialized data stores.

> **Interview:** An e-commerce application may use a relational database for orders, payments, and inventory integrity, with a cache or NoSQL store for selected workloads.
