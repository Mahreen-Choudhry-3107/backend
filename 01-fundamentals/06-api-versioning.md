# 06. API Versioning

API versioning allows a backend to evolve while existing clients continue using a compatible contract.

## Common strategies

- **URL:** `/api/v1/users` and `/api/v2/users`.
- **Query parameter:** `/api/users?version=2`.
- **Header-based versioning:** client specifies a version in a request header.
- **Media type versioning:** version is represented in the `Accept` media type.

## Best practices

- Prefer backward-compatible changes where possible.
- Document changes and migration steps.
- Define a deprecation policy and timeline.
- Monitor older-version usage before retirement.
- A new optional field does not necessarily require a new version.

> **Interview:** Introduce a new version when a change cannot remain backward compatible and clients need a separate contract or migration period.
