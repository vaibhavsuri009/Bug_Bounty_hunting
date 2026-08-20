# Web vs Mobile Security-Control Bypass

- What it is: The website enforces an extra authentication/security check that the mobile app omits.
- Reproduce the same risky login/action through browser and mobile/API clients.
- Use a new IP/device context to trigger the web-side protection.
- Compare required verification steps across platforms.
- The Twitter example found extra login verification on web but not mobile.
- Check whether the weaker channel exposes data that then bypasses the stronger channel too.
- False positive: mobile may be protected by device-bound credentials not visible in the UI.
- Edge case: third-party clients and legacy APIs can create additional inconsistent paths.
- Remediation: centralize security policy server-side across all clients.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
