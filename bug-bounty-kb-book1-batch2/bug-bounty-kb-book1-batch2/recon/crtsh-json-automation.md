# crt.sh JSON Automation

- What it is: Pull certificate-transparency results as JSON for automated hostname discovery.
- Where to look: Use when enumerating hostnames and Subject Alternative Names related to an in-scope domain.
- Query crt.sh with JSON output:
```bash
curl "https://crt.sh/?q=$DOMAIN&output=json" -o ${DOMAIN}_recon/crt
```
- Parse certificate hostnames from the `name_value` field:
```bash
jq -r '.[] | .name_value' ${DOMAIN}_recon/crt
```
- Feed discovered names into later subdomain validation/enumeration steps.
- Deduplicate results before further scanning when the same hostname appears in multiple certificates.
- False-positive/edge note: Certificate names can be stale, third-party, or out of scope; validate scope and DNS resolution first.
- Remediation: Certificate transparency is public by design; minimize unnecessary hostname exposure and retire obsolete DNS records.

## Source: Bug Bounty Bootcamp, Ch. 5
