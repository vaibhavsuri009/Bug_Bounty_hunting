# Application-Specific Payload Shape Inference

- What it is: Private/internal API payloads often do not follow public standards, so their expected object shape must be inferred.
- Where to look / how to identify it:
  - Start from known browser-generated requests, documentation hints, and verbose errors.
- Exploitation / test pattern:
  - Change one field at a time and record required names, allowed values, types, and nesting.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Network or Burp-like request inspection.
- Common false-positive / WAF / edge-case notes:
  - Generic errors can conceal the shape; avoid noisy blind brute force unless authorized.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use clear internal API specifications and strict schema validation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 5
