# Negative Price / Credit Business Logic Test

- What it is: A privileged product-creation or pricing API may accept negative prices and invert purchase accounting.
- Where to look / how to identify it:
  - Using a test store/account, identify a product-create/update endpoint; submit the documented required fields with a small negative test price; purchase only the controlled test item and verify balance behavior.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Creating a product is already a separate privilege issue; negative-price impact must be verified.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Enforce price bounds and restrict product management to authorized roles.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 11
