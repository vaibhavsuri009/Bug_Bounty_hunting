# Malformed Boolean-Attribute Sanitizer Bypass

- What it is: A sanitizer removes an attribute value but leaves parsing tokens that the browser reinterprets as new attributes.
- Look for HTML-capable inputs where some tags/attributes are allowed but JavaScript handlers are stripped.
- Test malformed Boolean attributes with unexpected values and inspect sanitized output.
```html
<INPUT TYPE="checkbox" CHECKED="hello" NAME="check box">
```
- Compare the sanitizer result with how the browser actually parses the DOM.
- The book's Yahoo example used attribute repair to expose a later event-handler attribute.
- False positive: strange rewritten markup is not enough; demonstrate a controllable executable attribute or meaningful DOM change.
- Edge case: browser HTML error-correction can differ from server-side sanitizer assumptions.
- Tools: DOM inspector to compare raw response vs parsed DOM.
- Remediation: use a proven HTML sanitizer that parses to a DOM/token stream rather than regex/string rewriting.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
