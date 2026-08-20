# GraphQL Sequential pID BOLA Test

- What it is: Sequential GraphQL object IDs can become BOLA targets when resolvers fail to verify ownership.
- Where to look / how to identify it:
  - Identify a resource ID such as `pId`, establish a known-good request for your own object, then test a second controlled object's ID.
- Exploitation / test pattern:
  - Use two controlled accounts/resources first; only expand testing inside scope after confirming the authorization model.
- Tools + exact CLI syntax (if mentioned):
  - Burp Repeater/Intruder can vary a numeric `pId` field in a controlled range.
- Common false-positive / WAF / edge-case notes:
  - A predictable ID is not itself a vulnerability; unauthorized access is the vulnerability.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Perform object-level authorization for every GraphQL resolver regardless of identifier complexity.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
