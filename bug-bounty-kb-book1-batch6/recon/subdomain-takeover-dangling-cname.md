# Dangling CNAME Subdomain Takeover

- **What it is:** A company subdomain still points to an unclaimed third-party resource that another user may be able to register.
- **Where to look:** Subdomains whose CNAME targets third-party hosting/services and return provider-specific unregistered-page errors.
- **Test / exploitation:**
  - Enumerate the target organization’s subdomains.
  - Resolve CNAME records and identify third-party-hosted targets.
  - Visit/screenshot each target and look for the provider’s unregistered-resource signature.
  - Confirm that the exact third-party resource can be claimed under program rules.
  - Host only a harmless proof page to demonstrate control.
- **Tools / syntax:**
```text
<html>Subdomain Takeover by YOUR_NAME.</html>
```
- **False positives / edge cases:**
  - A dangling CNAME alone is not enough; some providers prevent unauthorized claiming.
- **Remediation:** Remove dangling DNS records or reclaim/secure the referenced third-party resource.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
