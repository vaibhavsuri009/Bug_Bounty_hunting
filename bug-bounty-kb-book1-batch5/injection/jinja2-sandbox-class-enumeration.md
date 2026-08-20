# Jinja2 Sandbox Class Enumeration

- A Jinja2 SSTI may expose Python object internals even when direct `os` or `__import__` access is blocked.
- Enumerate subclasses reachable from the base `object` class:
```text
{{[].__class__.__bases__[0].__subclasses__()}}
```
- Breakdown: empty list -> its class -> base class (`object`) -> all loaded subclasses.
- Search the returned class list for useful already-loaded objects rather than trying a blocked import directly.
- Available subclasses vary by Python version and application environment, so class positions/names are not universal.
- Use this as an environment-enumeration step before any sandbox-escape attempt.
- False-positive trap: hardened Jinja sandboxes may block dunder attributes or object traversal entirely.
- The chapter uses this traversal because direct `__import__` access is typically unavailable in Jinja templates.
- Remediation: deny unsafe attribute access and do not evaluate untrusted template source.
## Source: Bug Bounty Bootcamp, Ch. 16
