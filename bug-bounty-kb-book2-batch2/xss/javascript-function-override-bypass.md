# JavaScript Function-Override Filter Bypass

- What it is: A client-side XSS defense disables selected functions, but JavaScript prototype behavior can restore/replace functionality.
- Look for security JavaScript that overrides `alert`, `confirm`, `prompt`, `document.write`, or similar functions.
- Read the site's scripts to identify what is blocked and what equivalent functions remain.
- The book describes restoring a native implementation from a prototype.
```javascript
document.write = HTMLDocument.prototype.write;
document.write('TEST');
```
- Use a harmless text write or `document.domain` alert to confirm bypass behavior.
- False positive: restoring a function does not prove attacker input can invoke it in an executable context.
- Edge case: properties made non-configurable or CSP restrictions can stop the approach.
- Remediation: never rely on client-side function blacklists as the primary XSS control; encode/sanitize at sinks.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
