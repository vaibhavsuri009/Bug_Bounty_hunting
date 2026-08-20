# XSS Polyglot Context Testing

- What it is: Polyglot payloads are designed to remain syntactically useful across multiple HTML/JavaScript contexts, reducing context-guessing effort.
- Where to look / how to identify it:
  - Use only benign lab-safe polyglots after identifying an unknown or variable reflection context.
- Exploitation / test pattern:
  - Observe which context executes and then replace the broad polyglot with a minimal proof.
- Tools + exact CLI syntax (if mentioned):
  - Browser/DevTools; the book references public polyglot research.
- Common false-positive / WAF / edge-case notes:
  - Polyglots are noisy and can trigger filters; they are discovery aids, not ideal final PoCs.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use context-aware encoding and safe DOM APIs across all rendering contexts.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
