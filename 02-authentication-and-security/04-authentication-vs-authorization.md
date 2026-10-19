# 04. Authentication vs Authorization

Authentication verifies identity; authorization decides what an identity may access or do.

## Authentication — who are you?

- Email and password login.
- Multi-factor authentication.
- Sign-in through an identity provider.
- API credentials for service-to-service calls.

## Authorization — what can you do?

- A user may view their own profile.
- An administrator may manage users.
- A manager may access reports for their team.
- A user may be blocked from modifying another user's records.

## Common authorization models

- **RBAC (Role-Based Access Control):** permissions are assigned to roles.
- **ABAC (Attribute-Based Access Control):** decisions depend on attributes such as ownership, department, or resource classification.
- **ACL (Access Control List):** specifies which identities or groups may perform actions on a resource.

## Security practices

- Enforce checks on the server, not only in the UI.
- Check resource ownership where needed.
- Follow least privilege and deny by default.
- Test for insecure direct object references, such as changing an ID to access another user's data.

> **Interview:** Successful login does not grant access to every endpoint. Each requested action and resource still needs an authorization check.
