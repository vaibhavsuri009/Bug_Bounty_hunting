# API Recon: Capture Workflows and Deduce Hidden Endpoints

- **What it is:** Enumerate undocumented APIs by recording real application workflows and inferring predictable routes.
- **Where to look:** Proxy history while exercising web/mobile features end to end.
- **Method:** Capture each API call, note resource/action naming, then infer sibling operations.
- **Examples from source:** If `/posts/ID/read` and `/posts/ID/delete` exist, test whether `/posts/ID/edit` exists; numeric gaps may reveal neighboring objects.
- **Also inspect:** JavaScript, public repositories, malformed-input errors, and API-specific wordlists.
- **False positives:** Guessed endpoints may exist but be intentionally inaccessible; validate authorization separately.
- **Remediation:** Remove deprecated/private endpoints and enforce identical controls on every route.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
