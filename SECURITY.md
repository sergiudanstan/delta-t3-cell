# Security Policy

This is a static, browser-only digital twin: one `index.html` with no backend, no
accounts, no cookies and no data sent anywhere. It loads three.js from the jsDelivr CDN
at a pinned version (`three@0.160.0`).

## Supported versions

| Version | Supported |
|---|---|
| 0.1.x | ✅ Current |

Single maintainer; only the latest release receives fixes.

## Reporting a vulnerability

**Please do not open a public issue for a security problem.** Report it privately:
**[Report a vulnerability](https://github.com/sergiudanstan/delta-t3-cell/security/advisories/new)**
(Security → Advisories → Report a vulnerability).

| Stage | Target |
|---|---|
| Acknowledgement | within 3 business days |
| Triage | within 10 business days |
| Fix, or a documented decision not to fix | within 90 days |

These are best-effort targets from a single unpaid maintainer, not a contractual SLA.
There is no bug bounty; credit is offered in the advisory and changelog.

## Scope

In scope: script injection through the page (for example through imported CSV or URL
parameters), the page loading code from any origin other than the pinned CDN URLs, and
anything in this repository's workflows that could publish a release not built from `main`.

Out of scope: vulnerabilities in three.js or the CDN itself (report upstream), and the
accuracy of the simulation — that is a correctness bug, file it as a normal issue.

## Supply chain

CI runs a headless page smoke test on every push, `npm audit` on the test tooling,
`pip-audit` on the hash-pinned CI toolchain, CodeQL, and `zizmor` on the workflows.
Actions are pinned to full commit SHAs and kept current by Dependabot. Releases attach a
source archive with Sigstore build provenance:

```
gh attestation verify delta-t3-cell-v0.1.0.tar.gz --repo sergiudanstan/delta-t3-cell
```
