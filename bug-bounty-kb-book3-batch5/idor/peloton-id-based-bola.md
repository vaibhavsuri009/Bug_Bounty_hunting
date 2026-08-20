# ID-Based BOLA in User Detail APIs

- What it is: User-detail endpoints can become BOLA when a consumer can substitute another user's ID and receive their records.
- Where to look / how to identify it:
  - Obtain IDs from two controlled accounts and request each resource while authenticated as the other user.
- Exploitation / test pattern:
  - Keep authentication constant and swap only the ID to demonstrate the authorization failure.
- Tools + exact CLI syntax (if mentioned):
  - Burp Repeater/Postman.
- Common false-positive / WAF / edge-case notes:
  - Sequential or visible IDs are not the issue by themselves.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Check authenticated identity against resource ownership on every object lookup.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
