# Payment Verification Parameter Bypass

- **What it is:** Client-controlled parameters make the server skip payment validation or treat an unverified method as already trusted.
- **Where to look:** Checkout requests containing flags such as saved_card, payment type, payment_id, amount, quantity, or verification state.
- **Test / exploitation:**
  - Capture a valid checkout request for each supported payment path.
  - Compare parameters used for saved versus newly entered payment methods.
  - Change or add the flag that selects the trusted/saved path while supplying an unverified payment value.
  - Submit only against your own test transaction and verify whether validation was skipped.
  - Check whether price, quantity, or payment-type fields are also trusted directly from the request.
- **False positives / edge cases:**
  - A successful HTTP response is not proof; verify the server actually accepted the transaction state.
- **Remediation:** Derive payment state and prices server-side and revalidate sensitive payment data at the authoritative step.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 17
