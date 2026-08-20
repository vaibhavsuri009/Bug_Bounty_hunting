# CSRF to Information Disclosure Chain

- **What it is:** Uses CSRF to change a destination setting so later sensitive information is sent to an attacker-controlled location.
- **Where to look:** Billing email, notification address, export destination, webhook, or report-recipient settings.
- Test whether the destination-setting endpoint is CSRF vulnerable.
- With your own test account, change the destination to a controlled address.
- Trigger or wait for a benign test report/notification and verify delivery.

```text
CSRF change destination -> application sends report -> controlled destination receives data
```

- **False positives / edge cases:** The destination change may require re-authentication or email confirmation, preventing the chain.
- **Remediation:** CSRF-protect sensitive preference changes and require confirmation for high-impact destination changes.

## Source: Bug Bounty Bootcamp, Ch. 9
