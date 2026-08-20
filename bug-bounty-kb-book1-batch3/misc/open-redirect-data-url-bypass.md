# Open Redirect Data URL Bypass

- **What it is:** Uses a `data:` URL to bypass redirect filters that expect only conventional web schemes.
- **Where to look:** Redirect parameters that accept arbitrary schemes or perform weak scheme validation.
- Test only where the application passes the value directly to browser navigation.

```text
data:text/plain,hello
```

- A `data:text/html` document can contain browser-executed HTML/JavaScript and may trigger a redirect.
- Base64 encoding can change what a simplistic filter sees.
- Verify whether the target/browser actually permits `data:` navigation in that context.
- **False positives / edge cases:** Modern browsers and CSP may block or constrain `data:` navigations.
- **Remediation:** Allow only explicitly required schemes, normally `https`, and validate the parsed destination origin.

## Source: Bug Bounty Bootcamp, Ch. 7
