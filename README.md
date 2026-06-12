# Kicbac Docs

Mintlify documentation for the Kicbac developer platform.

The docs cover tokenized payments, Collect.js hosted fields, Customer Vault, subscriptions, ACH, webhooks, SDKs, test mode, and the OpenAPI reference.

## Local preview

```sh
pnpm dlx mint dev
```

## Verification

```sh
pnpm run broken-links
pnpm run openapi-check
pnpm run validate
```

The OpenAPI file lives at `openapi/kicbac.openapi.yaml` because Mintlify validates paths from the docs project root.

## Content rules

- Use active voice and second person.
- Use actual SDK APIs from the published packages.
- Do not create raw card inputs or server-side raw PAN/CVV examples.
- Document `response=2` as a typed decline result and `response=3` as an exception/error path.
- Verify webhooks with `Webhook-Signature: t=<nonce>,s=<sig>` over `nonce + "." + rawBody`.
- Use only the public test data in `openapi/data/`.

## Deployment

Connect this repository to Mintlify and set the docs root to the repository root. No gateway credentials are required to build or preview the docs.
