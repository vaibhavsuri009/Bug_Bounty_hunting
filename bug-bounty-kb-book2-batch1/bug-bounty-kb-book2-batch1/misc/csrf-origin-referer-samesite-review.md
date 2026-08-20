# CSRF Origin, Referer, and SameSite Review

- What it is: Evaluate whether request-origin checks and cookie `SameSite` behavior actually block cross-site state changes.
- Where to look: State-changing endpoints that rely on `Origin`, `Referer`, or `SameSite` rather than only a CSRF token.
- Capture a legitimate request and note whether the server checks `Origin` first and/or falls back to `Referer`.
- Verify requests with missing or unexpected origin information are rejected rather than merely checked for header presence.
- Inspect authentication cookies for `SameSite` behavior.
- `Strict` should prevent the cookie being sent on cross-site requests.
- `Lax` can still send cookies on initial cross-site GET navigation, so GET endpoints must remain read-only.
- Compare top-level navigation behavior with form/image subrequests because browser cookie handling can differ.
- Check whether a state-changing GET remains possible under `SameSite=Lax`.
- Test only using browser-generated cross-site requests; remote JavaScript normally cannot arbitrarily set `Origin` or `Referer`.
- False-positive trap: A missing token is not exploitable if browser cookie rules or strict origin validation still block the action.
- Remediation: Combine robust CSRF tokens/origin validation with appropriate `SameSite` cookie settings.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 4
