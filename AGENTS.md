# Documentation project instructions

This Mintlify site documents Kicbac's developer platform. Follow the root `AGENTS.md` API and security rules.

## Content rules

- Use active voice and second person.
- Keep headings in sentence case.
- Code blocks need language tags.
- Internal links are root-relative and omit file extensions.
- Use actual SDK APIs from package READMEs and exports.
- Do not generate raw card inputs or server-side raw PAN/CVV examples.
- Document `response=2` as a typed decline result and `response=3` as an exception/error path.
- Verify webhooks with `Webhook-Signature: t=<nonce>,s=<sig>` over `nonce + "." + rawBody`.
- Use only test data from `openapi/data/*.json` and `todo.md` Appendix B.
