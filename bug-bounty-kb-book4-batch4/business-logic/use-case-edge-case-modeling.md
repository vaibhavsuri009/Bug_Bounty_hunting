# Use-Case Edge-Case Modeling

- What it is: A practical way to find logic flaws is to map intended user journeys and systematically challenge assumptions at each step.
- Where to look / how to identify it:
  - Write the normal workflow, backend assumptions, state transitions, external dependencies, and financial/data effects.
- Exploitation / test pattern:
  - Generate edge cases around limits, reversals, ownership, timing, currency, repetition, and role changes.
- Tools + exact CLI syntax (if mentioned):
  - Structured notes/checklists.
- Common false-positive / WAF / edge-case notes:
  - Many edge cases produce expected validation failures; only unexpected meaningful outcomes are findings.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Build abuse cases into requirements, threat models, and automated business-rule tests.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 18
