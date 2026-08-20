# Reflected XSS

- What it is: User input is immediately returned by the server into a page without safe output encoding.
- Where to look: Search terms, error messages, URL parameters, path components, and other request data reflected in responses.
- First inject a unique marker and confirm it appears in returned HTML.
- Then test an execution payload in the same parameter:
```text
https://example.com/search?q=<script>alert('XSS')</script>
```
- Inspect the response source to determine the HTML/attribute/JavaScript context before choosing a payload.
- Reproduce using a URL that another user could realistically open.
- False-positive/edge note: Reflection without executable context is not XSS.
- WAF/edge note: Different browsers can parse malformed HTML differently; verify in the intended browser context.
- Remediation: Apply context-sensitive output encoding and avoid inserting raw request data into HTML.

## Source: Bug Bounty Bootcamp, Ch. 6
