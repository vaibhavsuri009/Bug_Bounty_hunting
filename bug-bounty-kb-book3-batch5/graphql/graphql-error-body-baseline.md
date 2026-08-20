# GraphQL Error-Body Baseline

- What it is: GraphQL often returns HTTP 200 even when a query fails, so status code alone is a poor fuzzing signal.
- Where to look / how to identify it:
  - Create known-valid and known-invalid requests and record response body, length, error structure, and timing.
- Exploitation / test pattern:
  - Use those baselines to find outliers during fuzzing instead of filtering only by HTTP status.
- Tools + exact CLI syntax (if mentioned):
  - Burp Intruder + Comparer or Postman tests.
- Common false-positive / WAF / edge-case notes:
  - Uniform HTTP 200 responses are normal in many GraphQL implementations.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Return consistent errors and avoid verbose backend details.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
