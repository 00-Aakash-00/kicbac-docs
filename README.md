# Kicbac Docs

Mintlify documentation for the Kicbac developer platform.

## Local preview

```bash
pnpm install
cd docs
pnpm dlx mint dev
```

## Verification

```bash
cd docs
pnpm dlx mint broken-links
pnpm dlx mint openapi-check openapi/kicbac.openapi.json
```

The docs use the mirrored OpenAPI file under `docs/openapi/` because current Mintlify CLI releases block `../` paths from a docs project directory.
