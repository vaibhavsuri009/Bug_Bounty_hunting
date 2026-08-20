# HTML Context Breakout for XSS

- What it is: Close the surrounding HTML syntax so injected content can create a new executable element.
- Where to look: Input embedded inside quoted attributes or existing HTML elements.
- Example vulnerable template:
```html
<img src="USER_INPUT">
```
- Break out of the attribute/tag and create a script element:
```html
"/><script>alert(1)</script>
```
- Inspect the returned HTML to verify quotes and tags balance after injection.
- Use browser developer tools/console to identify syntax errors when a payload fails.
- Choose the breakout characters based on the exact context: quote type, attribute, and surrounding tag.
- False-positive/edge note: Seeing the payload text in source does not prove the browser parses it as executable markup.
- Remediation: Use context-aware attribute encoding and safe templating APIs.

## Source: Bug Bounty Bootcamp, Ch. 6
