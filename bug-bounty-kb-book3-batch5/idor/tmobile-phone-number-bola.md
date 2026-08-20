# Phone Number BOLA

- What it is: A predictable phone-number parameter can become a BOLA vector when one user token can retrieve other customers' account data.
- Where to look / how to identify it:
  - Use two controlled phone numbers/accounts and replay the request with the caller token unchanged.
- Exploitation / test pattern:
  - Swap only the target phone number and compare whether private account data is returned.
- Tools + exact CLI syntax (if mentioned):
  - Burp Repeater or Postman.
- Common false-positive / WAF / edge-case notes:
  - Phone numbers being predictable/public does not excuse missing authorization.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Authorize the target resource against the authenticated user, not against possession of the identifier.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
