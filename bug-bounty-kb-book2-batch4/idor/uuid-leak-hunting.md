# UUID Leakage Hunting for IDOR

- What it is: An otherwise unguessable identifier is disclosed elsewhere in the application.
- Search JSON responses, HTML source, invitation responses, search results, public share links, and URLs.
- Use a proxy to inspect data not rendered visibly in the UI.
- Once a UUID is found, test it with a lower-privileged controlled account.
- The book's ACME example leaked `customer_id` inside order-search JSON.
- Google dorks can also reveal public URLs containing identifiers.
- False positive: a leaked UUID is not itself a vulnerability if authorization remains correct.
- Edge case: revoked users may retain historical IDs that still work.
- Remediation: minimize identifier disclosure and enforce authorization independently.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 16
