# OWASP ZAP API URI Crawling

- What it is: ZAP crawls linked content and searches responses to discover API-related routes.
- Start ZAP → Quick Start → Automated Scan and enter the target URL.
- Monitor Spider/Sites results during the crawl.
- Search results for strings such as `API`, `GraphQL`, `JSON`, `RPC`, and `XML`.
- Use Manual Explore/HUD to browse authenticated or feature-specific areas.
- Treat colored alerts as leads and validate them manually.
- False positive: ZAP automated alerts can contain significant noise.
- Edge case: crawling will not find unlinked/hidden routes; combine it with brute force.
- Remediation: do not depend on links being hidden as a security control.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 6
