# Asynchronous Order Security Review

- What it is: Asynchronous callbacks, promises, and async/await can resolve in unexpected timing order and may expose race-like security mistakes.
- Where to look / how to identify it:
  - Look for security checks and state-changing operations split across asynchronous calls.
- Exploitation / test pattern:
  - Map the intended order: fetch identity → fetch resource → check authorization → update state; flag gaps where order can change.
- Tools + exact CLI syntax (if mentioned):
  - Source review, DevTools Performance/Network timing.
- Common false-positive / WAF / edge-case notes:
  - Variable timing alone is normal; prove a state or authorization decision can be bypassed.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use atomic server-side transactions and keep security checks coupled to state changes.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
