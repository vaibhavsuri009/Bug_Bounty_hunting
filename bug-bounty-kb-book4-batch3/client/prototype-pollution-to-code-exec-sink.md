# Prototype Pollution to Code-Execution Sink

- What it is: Prototype pollution becomes critical when a polluted property reaches a script-execution sink on the client or server.
- Where to look / how to identify it:
  - After proving harmless pollution, trace affected values into `eval`, dynamic DOM parsing, command construction, or similar sinks.
- Exploitation / test pattern:
  - Demonstrate only with non-destructive lab-safe output.
- Tools + exact CLI syntax (if mentioned):
  - Source tracing and controlled local execution.
- Common false-positive / WAF / edge-case notes:
  - Pollution without a reachable execution sink may have limited impact.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Eliminate dangerous sinks and validate object ownership/prototype keys.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 16
