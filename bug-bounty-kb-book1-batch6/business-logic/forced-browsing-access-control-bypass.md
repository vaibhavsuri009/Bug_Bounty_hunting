# Forced Browsing Access-Control Bypass

- **What it is:** A protected entry page exists, but deeper resources can be requested directly without the same authorization check.
- **Where to look:** Admin dashboards, workflow step URLs, report/download endpoints, and action URLs reached after an authenticated redirect.
- **Test / exploitation:**
  - Complete the normal flow and record each final resource URL.
  - Log out or switch to a low-privileged account.
  - Request the deeper URL directly instead of entering through the protected page.
  - Test direct GET and the underlying state-changing requests separately.
  - Confirm whether the resource or action succeeds without the expected authorization context.
- **False positives / edge cases:**
  - Client-side route protection or hidden navigation is not a security boundary.
- **Remediation:** Enforce authorization on every resource and action endpoint.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 17
