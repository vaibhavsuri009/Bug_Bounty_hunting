# High-Risk Interpreter Inventory

- What it is: Injection can target any interpreter, scheduler, logger, compiler, backup script, compression tool, database, or OS command wrapper.
- Where to look / how to identify it:
  - List server-side components that interpret user-influenced strings or commands.
- Exploitation / test pattern:
  - Prioritize these components for code review, parameter allowlists, and least privilege.
- Tools + exact CLI syntax (if mentioned):
  - Architecture/source review.
- Common false-positive / WAF / edge-case notes:
  - Merely invoking a CLI or interpreter is not a vulnerability if all arguments are safe and constrained.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Minimize interpreter exposure and isolate each execution boundary.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 31
