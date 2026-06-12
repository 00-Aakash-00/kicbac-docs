# Security policy

This repository contains documentation and public test fixtures. It must never contain live Kicbac credentials, webhook signing keys, raw card data, bank account numbers, or unscrubbed network recordings.

## Reporting a documentation security issue

Open an issue for ordinary documentation bugs. For anything involving leaked credentials, unsafe payment examples, webhook verification mistakes, or PCI-sensitive content, contact the Kicbac maintainers privately.

## Documentation guardrails

- Show Kicbac.js tokenization, not raw card fields.
- Use placeholders for keys and environment variables.
- Use only public test values from `openapi/data/`.
- Keep webhook verification byte-exact: HMAC-SHA256 over `nonce + "." + rawBody`.
- Keep declines documented as typed results, not exceptions.
