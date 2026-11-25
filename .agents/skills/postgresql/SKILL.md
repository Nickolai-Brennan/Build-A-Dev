---
name: postgresql
description: Design or review PostgreSQL schemas, SQL, migrations, indexes, transaction boundaries, and query plans.
---

# PostgreSQL

1. Identify the server major version, existing schema and migration runner. Define row grain, keys, constraints, and transaction boundaries before changing SQL.
2. Use bound values and the existing migration workflow. Check locking and old data compatibility before applying DDL. Verify correctness and plans on a disposable or approved nonproduction database.
3. Compare query results to known fixtures. Use EXPLAIN first and run EXPLAIN ANALYZE only when executing the statement is safe. Document rollout and recovery for migrations.

Report the files changed, verification run, and any unavailable environment or access.

[Product documentation](https://www.postgresql.org/docs/current/)
