# API Rate-Limit and Evasion Checklist

- What it is: Rate-limit testing determines whether limits exist, whether they are enforced, and whether simple request variants bypass them.
- Where to look / how to identify it:
  - Observe documented limits, `429` responses, retry headers, token/IP attribution, and path/header normalization.
- Exploitation / test pattern:
  - Throttle authorized tests and stop before creating availability impact.
- Tools + exact CLI syntax (if mentioned):
  - Book tools include Wfuzz delays and Burp Intruder Resource Pools.
- Common false-positive / WAF / edge-case notes:
  - A lax but intentional limit is not automatically a vulnerability; demonstrate security or business impact.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Centralize rate limiting on normalized identity and route keys and monitor abusive patterns.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. A
