# XSS Attribute Breakout with `autofocus` + `onfocus`

- What it is: A quote closes an existing HTML attribute and injects an event handler.
- Look for input rendered inside quoted attributes such as `value="USER_INPUT"`.
- Probe whether a double quote remains unescaped.
```text
hacker" onfocus=alert(document.domain) autofocus "
```
- Expected structure is an injected `onfocus` handler plus `autofocus`.
- `autofocus` can trigger the event automatically when the page loads.
- False positive: hidden inputs cannot be autofocus targets.
- Edge case: when multiple elements use autofocus, browser behavior may select the first or last.
- CSP/event-handler restrictions can also prevent execution.
- Remediation: HTML-attribute encode untrusted values and avoid constructing attributes by string concatenation.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
