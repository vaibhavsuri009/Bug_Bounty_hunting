# Smarty `{php}` Tag Code-Execution Proof

- What it is: Older/configured Smarty templates may allow embedded PHP tags to execute server-side PHP.
- Prerequisite: first confirm that attacker input is evaluated as Smarty template syntax.
- The book uses a benign print test:
```text
{php}print "Hello"{/php}
```
- If the downstream output contains `Hello`, PHP execution capability is demonstrated.
- Use a harmless deterministic function for proof; do not run destructive commands.
- False positive: modern Smarty versions/configurations may disable `{php}` entirely.
- Edge case: a template may parse Smarty syntax while restricting PHP tags.
- Document the exact Smarty version and rendering workflow.
- Remediation: disable PHP execution in templates, upgrade Smarty, and treat all user input strictly as data.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
