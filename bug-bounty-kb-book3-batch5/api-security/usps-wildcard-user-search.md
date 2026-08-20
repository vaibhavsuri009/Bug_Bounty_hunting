# Wildcard Search Data Exposure

- What it is: Search APIs can expose large user populations when wildcard queries are accepted without proper authorization or result limiting.
- Where to look / how to identify it:
  - Test wildcard behavior only with authorized test data and verify whether the API returns more records than the caller should access.
- Exploitation / test pattern:
  - Compare exact-match queries with wildcard queries and inspect returned identity fields.
- Tools + exact CLI syntax (if mentioned):
  - Example pattern from the book: search terms using `*` as a wildcard.
- Common false-positive / WAF / edge-case notes:
  - Wildcard support can be legitimate; the problem is unrestricted sensitive data access.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Apply authorization before search, restrict wildcard scope, and minimize returned fields.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
