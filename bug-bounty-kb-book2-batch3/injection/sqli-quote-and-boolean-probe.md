# SQLi Quote + Boolean Probe

- What it is: User input is concatenated into a SQL query without safe parameterization.
- Look for URL/form parameters that appear to influence database-backed results.
- Start by comparing normal input with a quote and a Boolean condition.
```text
test' OR 1='1
```
- A result-set change or SQL error can indicate the parameter reached query syntax.
- Compare true and false conditions rather than relying on one response.
- Use application-specific values so the baseline query is predictable.
- False positive: result changes can come from application validation rather than SQL evaluation.
- Edge case: operator precedence may keep later `AND` conditions effective.
- Remediation: use prepared statements/parameterized queries, not string concatenation.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
