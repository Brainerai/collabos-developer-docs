# CollabOS Developer Docs

Official developer documentation for the CollabOS API.

This repository contains the guides and API reference for developers building personal integrations, workspace integrations, and webhook consumers with CollabOS.

## What's covered

- Getting started and authentication
- Personal and workspace API keys
- API scopes and permissions
- Raffles, entries, wins, winners, and projects
- Cursor pagination and rate limits
- Machine-readable errors
- API key management
- Webhook events, signatures, retries, and delivery history
- OpenAPI-powered API reference

## API reference

The API reference is generated from:

```text
openapi/developer-api.json
```

The backend OpenAPI contract is the source of truth for endpoint paths, request parameters, response schemas, authentication requirements, and error contracts.

## Project structure

```text
.
├── docs.json
├── favicon.svg
├── index.mdx
├── quickstart.mdx
├── guides/
├── webhooks/
└── openapi/
    └── developer-api.json
```

## Local development

Install the Mintlify CLI and run the docs from the repository root:

```bash
mintlify dev
```

## Updating the API reference

When the Developer API changes:

1. Update the backend implementation and tests.
2. Regenerate the backend OpenAPI contract.
3. Sync the generated `developer-api.json` into this repository.
4. Update any affected guides or examples.
5. Preview the docs before publishing.

Do not manually redefine endpoint schemas in MDX pages. Keep exact API contracts in OpenAPI and use the guides for workflows, examples, and explanations.
