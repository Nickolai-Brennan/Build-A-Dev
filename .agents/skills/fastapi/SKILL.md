---
name: fastapi
description: Implement or review FastAPI routes, Pydantic contracts, dependency injection, OpenAPI, and ASGI tests.
---

# FastAPI

1. Find routers, Pydantic version, lifespan setup, dependency overrides, and existing OpenAPI and errors. Keep response and status compatibility for callers.
2. Use request and response models at the boundary and reuse application services. Match sync or async execution to the driver and avoid blocking the event loop.
3. Exercise the route via the existing ASGI test harness. Verify example success, invalid input, and absent or unauthorized data where relevant, then inspect generated OpenAPI.

Report the files changed, verification run, and any unavailable environment or access.

[Product documentation](https://fastapi.tiangolo.com/tutorial/testing/)
