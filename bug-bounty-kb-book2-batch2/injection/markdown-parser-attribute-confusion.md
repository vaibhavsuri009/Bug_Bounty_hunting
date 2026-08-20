# Markdown Parser Attribute Confusion

- What it is: Extra quotes/attribute-like text can confuse Markdown parsing and produce unintended HTML attributes.
- Look for Markdown links that accept a URL plus a quoted title.
- Begin from normal syntax, then add extra quotes and attribute-looking tokens.
```markdown
[test](https://example.test "test ismap="marker" yyy="test"")
```
- Inspect generated HTML rather than relying only on rendered appearance.
- A strong signal is parser output containing attributes that were never intended by the Markdown grammar.
- This is useful when retesting a newly deployed Markdown fix.
- False positive: arbitrary attributes alone may not have executable impact; determine whether dangerous attributes/tags can actually be produced.
- Edge case: parser versions and post-processing sanitizers can alter the result.
- Tools: page source / DOM inspector.
- Remediation: upgrade the Markdown parser and sanitize its generated HTML before insertion.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 5
