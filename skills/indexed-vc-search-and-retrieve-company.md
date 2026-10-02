---
name: indexed-vc-search-and-retrieve-company
description: Search for a company and retrieve its full details by slug.
api: openapi/indexed-vc-openapi.yaml
operations:
- searchCompanies
- getCompany
generated: '2026-10-02'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/indexed-vc-openapi.yaml ; every operationId checked against the contract
---

# indexed-vc-search-and-retrieve-company

Search for a company and retrieve its full details by slug.

## Steps

1. 1. Use `searchCompanies` with query parameters such as `q` or `industry` as defined in the contract.
2. 2. From the search results, take the `slug` of the desired company.
3. 3. Use `getCompany` with the path parameter `{slug}` to fetch the company's full profile.

## Rules

- Auth: Include the API key in the `X-API-Key` header (ApiKeyAuth).
- Idempotency: GET operations (`searchCompanies`, `getCompany`) are safe and can be retried without side effects.
