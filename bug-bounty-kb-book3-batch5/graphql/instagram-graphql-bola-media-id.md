# GraphQL Media-ID BOLA

- What it is: A GraphQL API can expose private media when authorization is missing for a caller-supplied media identifier.
- Where to look / how to identify it:
  - Use controlled private media objects and test whether another controlled account can request the object by media ID.
- Exploitation / test pattern:
  - Keep the caller identity fixed and change only the media identifier or token field to isolate the control failure.
- Tools + exact CLI syntax (if mentioned):
  - Burp Repeater/Postman GraphQL.
- Common false-positive / WAF / edge-case notes:
  - Being able to request public media is expected; prove the resource is private and belongs to another user.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Enforce object-level authorization in the GraphQL resolver before returning media details.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
