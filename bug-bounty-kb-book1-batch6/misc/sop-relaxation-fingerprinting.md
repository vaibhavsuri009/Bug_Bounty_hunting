# SOP Relaxation Fingerprinting

- **What it is:** Identifies whether an application relaxes the Same-Origin Policy through CORS, postMessage, or JSONP.
- **Where to look:** HTTP responses and client-side JavaScript during normal browsing.
- **Test / exploitation:**
  - Proxy traffic and search responses for Access-Control-Allow-Origin.
  - Inspect page event listeners for message handlers.
  - Search script tags for callback/jsonp parameters.
  - Map each cross-origin data flow and identify whether it carries authenticated or sensitive data.
  - Test the mechanism-specific validation only after confirming its use.
- **False positives / edge cases:**
  - Cross-origin communication is not automatically vulnerable; the security check must be weak or missing.
- **Remediation:** Use strict origin validation and minimize cross-origin exposure.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 19
