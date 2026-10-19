# 03. HTTP Methods & Status Codes

HTTP methods express the intended action on a resource. Status codes communicate the outcome of a request.

## Common methods

- **GET:** retrieve a representation without intending to change server state.
- **POST:** submit data for processing, commonly to create a resource.
- **PUT:** generally replace the target resource representation.
- **PATCH:** apply partial modifications.
- **DELETE:** request removal of the target resource.

## Idempotency

- An operation is idempotent if repeating the same request has the same intended effect on server state as doing it once.
- GET, PUT, and DELETE are defined as idempotent, although response codes may differ.
- POST is not inherently idempotent. Use idempotency keys for operations such as payment creation when duplicate effects must be avoided.

## Success codes

- `200 OK` — request succeeded.
- `201 Created` — resource created.
- `202 Accepted` — accepted for processing, which may not be complete.
- `204 No Content` — succeeded without a response body.

## Client and server errors

- `400 Bad Request` — malformed or invalid request.
- `401 Unauthorized` — authentication is missing or unsuccessful.
- `403 Forbidden` — request is refused, often due to permissions.
- `404 Not Found` — resource not found.
- `409 Conflict` — conflict with current state.
- `422 Unprocessable Content` — semantically invalid content.
- `429 Too Many Requests` — rate limit exceeded.
- `500 Internal Server Error` — unexpected server failure.
- `502 Bad Gateway` — invalid upstream response.
- `503 Service Unavailable` — temporarily unavailable.
- `504 Gateway Timeout` — upstream did not respond in time.

> **Interview:** 401 generally indicates missing or invalid authentication; 403 means the server refuses access. PUT generally replaces a resource, while PATCH applies partial changes.
