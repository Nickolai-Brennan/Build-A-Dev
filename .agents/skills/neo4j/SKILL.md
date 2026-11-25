---
name: neo4j
description: Model Neo4j property graphs, implement parameterized Cypher, and review constraints, imports, and traversal performance.
---

# Neo4j

1. Confirm server version, database, labels, relationship types/direction, stable keys, and driver conventions. Define constraints before using MERGE for repeatable writes.
2. Bind user values, group writes in appropriate transactions, and bound path traversals. Verify node and edge cardinality before bulk imports.
3. Test create, duplicate import, and traversal on a small fixture. Use EXPLAIN before profiling and treat PROFILE as execution when selecting a safe environment.

Report the files changed, verification run, and any unavailable environment or access.

[Product documentation](https://neo4j.com/docs/cypher-manual/current/)
