---
name: api-contracts
description: Design, implement, or review an HTTP API endpoint and its frontend contract. Use when wiring a web app to a backend or specifying OpenAPI schemas, validation, response types, and API errors.
---

# Define an HTTP API contract

1. Identify the caller, resource, verb, expected data, and whether the operation reads or changes state. Inspect existing routes, models, authorization, and error conventions.
2. Specify request and response fields, types, nullability, units, status codes, and one example. Document empty results, invalid inputs, and authorization failures where applicable.
3. Reuse the backend service and its typed schema. For UI integration, align the consumer's types and empty and error states with the contract. Keep service credentials server-side.
4. Verify a representative request, invalid input, and an empty or absent result through the normal entry point. Check that existing callers continue to receive compatible responses or document the intended migration.
5. Return the route, contract location, example request, test command, and actual verification status. If implementation or execution is unavailable, provide the spec and identify the missing prerequisite.
