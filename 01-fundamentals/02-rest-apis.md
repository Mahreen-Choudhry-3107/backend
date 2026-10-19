# 02. REST APIs

REST (Representational State Transfer) is an architectural style for networked applications. A REST API commonly exposes resources through URLs and uses HTTP semantics to retrieve or modify them.

## Example endpoints

- `GET /api/products` — list products.
- `GET /api/products/101` — retrieve product 101.
- `POST /api/products` — create a product.
- `PATCH /api/products/101` — update selected fields.
- `DELETE /api/products/101` — request removal of a product.

## Important REST principles

- **Client–server separation:** frontend and backend have distinct responsibilities.
- **Statelessness:** each request carries the context needed to process it; the server should not depend on previous request context.
- **Cacheability:** responses can specify whether they may be cached.
- **Uniform interface:** resources are accessed through consistent conventions.
- **Layered system:** gateways, proxies, and other intermediaries may sit between client and server.
- **Code on demand** is optional.

## Good API practices

- Use nouns for resources and consistent URL conventions.
- Use HTTP methods according to their semantics.
- Return meaningful status codes and consistent error structures.
- Validate inputs and enforce authorization on the server.
- Support pagination for large collections.
- Document compatibility and versioning decisions.

> **Interview:** HTTP is a communication protocol; REST is an architectural style that can use HTTP. Not every HTTP API is RESTful.
