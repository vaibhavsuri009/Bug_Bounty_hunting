# CSRF Protection Bypass via XSS

- **What it is:** A same-origin XSS can read anti-CSRF data and issue authenticated state-changing requests.
- **Where to look:** Applications where an XSS exists on the same origin as token-protected sensitive actions.
- Use the XSS context to read the legitimate CSRF token from the DOM or page state.
- Then send the state-changing request from same-origin JavaScript using the valid token.
- This is a vulnerability chain: the XSS is the prerequisite.

```text
XSS -> read CSRF token -> same-origin request -> state change
```

- **False positives / edge cases:** HttpOnly affects cookies, not tokens rendered into the page; CSP may constrain script execution but does not fix an existing exploitable XSS by itself.
- **Remediation:** Fix XSS at the source and retain independent CSRF defenses as defense-in-depth.

## Source: Bug Bounty Bootcamp, Ch. 9
