---
name: provision-users-with-scim
description: Create, query, update and deprovision BigPanda users and groups over the SCIM 2.0 surface — the standards-based path an IdP already speaks.
api: bigpanda:bigpanda-users-api
generated: '2026-09-04'
method: generated
source: openapi/bigpanda-users-api-openapi.yml
operations:
  - createUserSCIM
  - getUsersBySCIMQueryParams
  - getUserByIdSCIM
  - updateUserByIdSCIM
  - patchUserByIdSCIM
  - createGroupSCIM
  - getGroupsBySCIMQueryParams
  - getGroupByIdSCIM
  - updateGroupByIdSCIM
  - patchGroupByIdSCIM
  - deleteGroupByIdSCIM
---

# Provision BigPanda users and groups over SCIM 2.0

Base URL `https://api.bigpanda.io`. `Authorization: Bearer <User API Key>` whose role carries user
administration permission.

BigPanda implements the standard SCIM 2.0 resource model, so an IdP that already provisions to Okta,
Entra ID or OneLogin needs no bespoke connector.

## Resources

| Resource | Path | Methods |
|---|---|---|
| Users | `/scim/v2/Users` | `POST` create, `GET` query |
| User | `/scim/v2/Users/{user_id}` | `GET`, `PUT` replace, `PATCH` modify |
| Groups | `/scim/v2/Groups` | `POST` create, `GET` query |
| Group | `/scim/v2/Groups/{group_id}` | `GET`, `PUT` replace, `PATCH` modify, `DELETE` |

Responses are returned as `application/scim+json`.

## Steps

1. **Query before you create.** `getUsersBySCIMQueryParams` — `GET /scim/v2/Users` with SCIM filter
   parameters. There is no idempotency key, so a blind `POST` on a retry creates a duplicate user.
2. **Create.** `createUserSCIM` — `POST /scim/v2/Users`.
3. **Modify incrementally** with `patchUserByIdSCIM` (`PATCH`) rather than replacing the whole record
   with `updateUserByIdSCIM` (`PUT`), so you do not clobber attributes another system owns.
4. **Groups mirror users**: `createGroupSCIM`, `getGroupsBySCIMQueryParams`, `patchGroupByIdSCIM`,
   `deleteGroupByIdSCIM`.

## Rules that matter

- **Rate limit: 2 requests per ROUTE per second** — tighter than the platform default of 5/second, and
  measured per path. A bulk sync that pages `/scim/v2/Users` and `/scim/v2/Groups` in parallel gets two
  independent budgets; hammering one path does not.
- **`DELETE` exists for Groups, not for Users.** Deprovision a user by patching their state rather than
  deleting the record; `/resources/v2.1/users/{user_id}` and the `UserStateFilter` enum are the
  BigPanda-native path.
- **Schemas are not published.** BigPanda's own spec marks the SCIM request and response bodies
  "Schema pending: definition lives in unbundled source-repo files." Build against RFC 7643 core
  schemas and validate against a live response before going to production.
- **SSO is configured separately** — see `/resources/v2.1/sso-config` and `/resources/v2.1/saml-debug`
  in `openapi/bigpanda-sso-provisioning-api-openapi.yml`. `saml-debug` validates a configuration without
  committing it, which is the nearest thing to a dry run in the surface.

## Sources
- https://api-docs.bigpanda.io/users
- https://api-docs.bigpanda.io/create-scim-group-37770146e0.md
