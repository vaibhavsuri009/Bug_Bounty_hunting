# XSS Bypass: Filter Recomposition

- What it is: Exploit filters that remove dangerous substrings only once, causing remaining fragments to join into valid markup.
- Where to look: Sanitizers that delete `<script>` strings rather than parsing and encoding HTML safely.
- Nested-tag test pattern:
```html
<scrip<script>t>alert(1)</scrip</script>t>
```
- If the filter strips only the inner intact tags, the remaining fragments can recombine into a valid `<script>` element.
- Compare input, server response, and final DOM to understand each transformation step.
- Repeat with harmless `alert(1)` or equivalent proof of execution.
- False-positive/edge note: Some browsers/frameworks normalize malformed markup differently; confirm reliable execution.
- Remediation: Do not sanitize with one-pass substring deletion; use proven HTML sanitizers plus context-aware encoding.

## Source: Bug Bounty Bootcamp, Ch. 6
