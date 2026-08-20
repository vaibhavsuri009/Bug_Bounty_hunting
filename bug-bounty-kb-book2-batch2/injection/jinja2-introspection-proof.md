# Jinja2 Introspection as SSTI Impact Proof

- What it is: Once Jinja2 expression execution is confirmed, template-object introspection can reveal accessible properties.
- First prove evaluation with a harmless arithmetic/loop expression.
- The book recommends stopping at a safe capability demonstration rather than causing unintended actions.
- Inspect only enough template/object properties to establish that code-capable primitives are reachable.
- Record the exact render context and downstream service performing evaluation.
- Do not escalate to destructive commands or sensitive-data access without explicit program authorization.
- False positive: arithmetic alone does not automatically prove arbitrary Python/RCE capability.
- Edge case: Jinja2 Sandbox and application-specific restrictions may block dangerous attributes.
- Tools: framework documentation plus controlled template expressions.
- Remediation: do not render user input as template source; enable sandboxing only as defense in depth.
- Prefer read-only introspection primitives and stop once the reachable object surface is demonstrated.
- Capture the evaluated output as evidence that the server, not the browser, processed the expression.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
