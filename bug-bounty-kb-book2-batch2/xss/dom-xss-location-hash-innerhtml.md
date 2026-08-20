# DOM XSS via `location.hash` to `innerHTML`

- What it is: Client JavaScript copies attacker-controlled URL-fragment data into an HTML sink.
- Look for DOM code assigning `location.hash`, `location.search`, or similar values to `innerHTML`.
```javascript
document.getElementById('name').innerHTML =
  location.hash.split('#')[1];
```
- A safe origin-confirmation probe from the book is:
```text
#<img src=x onerror=alert(document.domain)>
```
- URL fragments are processed client-side and are not normally sent to the server.
- False positive: `textContent`/proper sanitization prevents markup interpretation.
- Edge case: browser URL encoding may require client-side decoding before the payload becomes markup.
- Tools: browser DevTools, DOM/source inspection.
- Remediation: use `textContent` for untrusted text or sanitize before writing to HTML sinks.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
