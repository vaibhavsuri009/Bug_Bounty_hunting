# Exposed Admin Panel Discovery

- **What it is:** Sensitive administrative functionality is reachable because its URL is hidden rather than properly access-controlled.
- **Where to look:** Obscure paths, alternate ports, development endpoints, encoded directory names, archived URLs, and unlinked admin routes.
- **Test / exploitation:**
  - Enumerate likely admin paths during recon.
  - Use URL brute forcing and search-engine/archived URL discovery to find unlinked routes.
  - Request discovered admin endpoints unauthenticated and as a low-privileged user.
  - Also request the final dashboard/action URLs directly instead of only the login page.
  - Treat exposure as exploitable only when sensitive functionality or data is actually reachable.
- **False positives / edge cases:**
  - A visible login page alone is not broken access control.
- **Remediation:** Apply authentication and authorization to every admin route and action, regardless of discoverability.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 17
