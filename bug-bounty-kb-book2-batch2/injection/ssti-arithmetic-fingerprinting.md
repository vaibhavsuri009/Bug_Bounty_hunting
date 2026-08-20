# SSTI Arithmetic Fingerprinting

- What it is: Template syntax supplied by the user is evaluated by the server instead of rendered literally.
- Identify likely template technology first with Wappalyzer, BuiltWith, headers, errors, or source clues.
- Submit a harmless arithmetic expression using the engine's syntax.
```text
{{7*7}}
```
- If the output becomes `49`, the expression was evaluated.
- Test every place the value is rendered, including emails and secondary services.
- Different engines use different syntax; ERB, Smarty, Jinja2, Liquid, and others are not interchangeable.
- False positive: the string `49` may already exist; use unique arithmetic and compare control requests.
- Edge case: input filters may allow arithmetic but block security-sensitive primitives, limiting impact.
- Remediation: never treat untrusted values as template source; pass them only as data variables.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
