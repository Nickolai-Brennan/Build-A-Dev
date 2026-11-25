---
name: authzed
description: Design or review AuthZed SpiceDB schemas, relationships, permission checks, and consistency for application authorization.
---

# AuthZed / SpiceDB

1. Map subject, resource, tenant, and action to namespaced object types, relations, and computed permissions. Confirm the actual access policy and required consistency.
2. Plan relationship writes and deletes alongside application changes. Use check results and appropriate consistency tokens when fresh grants or revocations matter. Handle errors without granting access.
3. Run schema validation and explicit allow, deny, and cross-tenant cases against an isolated instance or approved fixture. Test grant/revoke freshness where the application depends on it.

Report the files changed, verification run, and any unavailable environment or access.

[Product documentation](https://authzed.com/docs/spicedb/concepts/schema)
