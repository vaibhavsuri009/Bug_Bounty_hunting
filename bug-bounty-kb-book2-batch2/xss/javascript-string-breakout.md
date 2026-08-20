# JavaScript String-Context Breakout

- What it is: User input inside a JavaScript string closes the quote and injects a new statement.
- Look for values rendered directly inside `<script>` blocks or inline JavaScript.
- Identify the surrounding quote type before crafting a probe.
```javascript
var name = 'USER_INPUT';
```
```text
hacker';alert(document.domain);'
```
- Preserve valid syntax after the injected statement so the page still parses.
- Inspect the rendered source because HTML-tag payloads may be encoded while JavaScript quotes remain unsafe.
- False positive: a reflected quote is harmless if it is JavaScript-string escaped (`\'`, JSON encoding, etc.).
- Edge case: CSP can block inline script execution even when the string is injectable.
- Remediation: serialize data with a safe JavaScript/JSON encoder rather than concatenating it into script.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
