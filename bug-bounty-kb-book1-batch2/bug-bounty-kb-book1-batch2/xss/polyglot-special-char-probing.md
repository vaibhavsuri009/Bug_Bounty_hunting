# XSS Polyglot and Special-Character Probing

- What it is: Use multi-context payloads or character probes to learn how an application transforms potential XSS syntax.
- Where to look: Unknown output contexts or filters whose exact behavior is unclear.
- Start with a generic special-character probe:
```text
>'<"//:=;!--
```
- Observe which characters are escaped, stripped, normalized, or returned unchanged.
- Build a context-specific payload only from characters that survive the filter.
- A polyglot combines several XSS syntaxes so one string may execute in multiple HTML contexts.
- Use polyglots for discovery, then minimize the final proof of concept to the simplest reliable payload.
- False-positive/edge note: A polyglot may trigger parser quirks not representative of realistic application flow; reproduce cleanly.
- Remediation: Encode by output context rather than relying on blocklists of specific payload strings.

## Source: Bug Bounty Bootcamp, Ch. 6
