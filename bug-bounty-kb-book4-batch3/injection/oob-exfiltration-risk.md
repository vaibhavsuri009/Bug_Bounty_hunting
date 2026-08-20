# Out-of-Band Injection Callback Risk

- What it is: When interpreter results are not returned in-band, some environments allow controlled outbound network callbacks from the interpreter.
- Where to look / how to identify it:
  - Assess whether the database/interpreter has outbound network capabilities and whether egress is restricted.
- Exploitation / test pattern:
  - Use a unique harmless callback token in a lab rather than transferring sensitive data.
- Tools + exact CLI syntax (if mentioned):
  - Controlled HTTP/DNS callback logging.
- Common false-positive / WAF / edge-case notes:
  - Outbound callbacks can originate from unrelated services; correlate unique test identifiers.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Restrict database/application egress and remove unnecessary network-capable functions.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 13
