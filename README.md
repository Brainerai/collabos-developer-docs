# CollabOS Developer Docs

A lightweight Mintlify documentation package for the CollabOS Developer API.

## What is included

- Human-readable getting-started and integration guides
- Personal and workspace API guidance
- Authentication, scopes, pagination, errors, and rate limits
- API-key management guidance
- Webhook events, signatures, retries, and testing
- `openapi/developer-api.json` as the API reference source of truth
- Mintlify `docs.json` navigation that generates reference pages directly from OpenAPI

## Before publishing

The exported OpenAPI contract does not include a `servers` entry, so the guides intentionally use `https://YOUR_API_BASE_URL` rather than inventing a production API hostname.

When the production API origin is confirmed, either:

1. Replace the placeholder in the guide examples, and
2. Add the production server to `openapi/developer-api.json` (preferably in the backend OpenAPI source-of-truth, then regenerate it).

The Mintlify playground is set to `simple` until a server URL is defined.

## Local preview

Install the current Mintlify CLI and run it from this directory using Mintlify's standard local-development command for your installed CLI version.

## Maintenance

Do not manually fork endpoint schemas into the MDX guides. Update the backend OpenAPI contract first, regenerate `openapi/developer-api.json`, then copy/sync the updated spec into this docs project. The MDX pages should explain how to use the API; OpenAPI should remain the exact endpoint/schema reference.
