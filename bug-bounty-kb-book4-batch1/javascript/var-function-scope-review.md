# JavaScript `var` Function-Scope Review

- What it is: `var` binds to the nearest function rather than the nearest block, which can create unexpected state and logic behavior.
- Where to look / how to identify it:
  - During source review, flag security-sensitive variables declared with `var` inside conditionals or loops.
- Exploitation / test pattern:
  - Trace whether the value remains accessible outside the intended block and affects authentication, authorization, or filtering.
- Tools + exact CLI syntax (if mentioned):
  - Manual source review.
- Common false-positive / WAF / edge-case notes:
  - Most `var` usage is a correctness concern rather than a vulnerability.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer `let` or `const` and use linting rules that reject accidental broad scope.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
