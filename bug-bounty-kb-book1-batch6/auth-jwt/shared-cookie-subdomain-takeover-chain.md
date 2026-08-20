# Shared-Cookie + Subdomain Takeover Chain

- **What it is:** A takeover of one subdomain can expose a parent-domain session cookie shared across multiple services.
- **Where to look:** SSO cookies with a Domain attribute such as example.com combined with a controllable subdomain.
- **Test / exploitation:**
  - Confirm a cookie is scoped to the parent domain in Set-Cookie.
  - Confirm a subdomain takeover using a harmless page.
  - Log in only with your own test account.
  - Visit the controlled subdomain and inspect whether the parent-domain cookie is sent.
  - If it is sent, document the cross-service session exposure without using another user’s cookie.
- **Tools / syntax:**
```text
Set-Cookie: cookie=abc123; Domain=example.com; Secure; HttpOnly
```
- **False positives / edge cases:**
  - Host-only cookies are not automatically sent to sibling subdomains.
- **Remediation:** Avoid broad parent-domain session cookies and eliminate takeover-prone DNS records.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
