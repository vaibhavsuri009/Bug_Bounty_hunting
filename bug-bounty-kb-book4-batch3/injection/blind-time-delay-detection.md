# Blind Time-Delay Injection Detection

- What it is: Blind injection can be inferred when a payload causes a deterministic processing delay without returning query results.
- Where to look / how to identify it:
  - Establish a latency baseline and use a small, harmless conditional delay in a controlled environment.
- Exploitation / test pattern:
  - Repeat enough times to distinguish application delay from ordinary network jitter.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Timing or proxy timing metrics.
- Common false-positive / WAF / edge-case notes:
  - Network congestion creates false positives; compare statistically and keep delays short.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Parameterize interpreter input and set query/runtime timeouts.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 13
