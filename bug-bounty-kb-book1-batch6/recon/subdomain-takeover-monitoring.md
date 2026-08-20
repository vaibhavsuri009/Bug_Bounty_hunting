# Continuous Subdomain Takeover Monitoring

- **What it is:** Periodically checks known subdomains for newly introduced dangling CNAMEs and unregistered third-party resources.
- **Where to look:** Large bug-bounty scopes where DNS and third-party hosting change over time.
- **Test / exploitation:**
  - Maintain a current subdomain inventory.
  - Periodically resolve CNAME targets and classify third-party providers.
  - Request hosted pages and match provider-specific unregistered-page signatures.
  - Alert only on suspected takeover candidates for manual verification.
  - Add newly discovered subdomains to the monitored set.
- **Tools / syntax:**
```text
30 10 * * * cd /Users/vickie/scripts/security; ./subdomain_takeover.sh
```
- **False positives / edge cases:**
  - Provider error pages and takeover eligibility can differ; manually verify before reporting.
- **Remediation:** Continuously inventory DNS and remove stale external-service mappings.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
