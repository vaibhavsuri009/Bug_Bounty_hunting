# API Hacking Master Checklist

- What it is: The book consolidates its methodology into a repeatable sequence: scope, recon, endpoint analysis, authentication, fuzzing, authorization, mass assignment, injection, rate limits, and evasion.
- Where to look / how to identify it:
  - Use the checklist to prevent major test areas from being skipped while still adapting to the target's documented scope.
- Exploitation / test pattern:
  - Record completed checks and findings so later chains can reuse earlier discoveries.
- Tools + exact CLI syntax (if mentioned):
  - Suggested order: approach → passive recon → active recon → endpoint analysis → auth → fuzzing → authorization → mass assignment → injection → rate limits/evasion.
- Common false-positive / WAF / edge-case notes:
  - A checklist is not a license to run disruptive tests; program rules remain authoritative.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Organizations should use the same categories defensively in continuous API security testing.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. A
