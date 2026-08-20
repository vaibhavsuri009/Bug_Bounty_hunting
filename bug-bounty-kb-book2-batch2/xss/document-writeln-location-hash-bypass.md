# XSS Filter Bypass with `document.writeln` + URL Fragment

- What it is: A blocked DOM-writing function has an unblocked equivalent, and the payload is carried in `location.hash`.
- Look for client defenses that disable `document.write` but leave `document.writeln` available.
- The book's pattern writes a decoded fragment into the DOM.
```javascript
document.writeln(decodeURI(location.hash))
```
- Put only a benign HTML execution marker after `#`.
```text
#<img src=1 onerror=alert(document.domain)>
```
- Fragments are not sent to the server, which may bypass server-side filtering of the payload body.
- False positive: writing the fragment as text rather than HTML prevents XSS.
- Edge case: decoding behavior and CSP can alter execution.
- Remediation: remove unsafe DOM sinks and validate/encode fragment-derived data before DOM insertion.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
