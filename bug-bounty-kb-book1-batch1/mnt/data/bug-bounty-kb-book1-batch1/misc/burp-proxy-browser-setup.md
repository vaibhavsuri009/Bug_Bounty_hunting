# Burp Browser + Proxy Setup

- What it is: Route browser traffic through Burp so HTTP requests/responses can be inspected and modified.
- Use Burp's embedded browser for zero-config proxying, or configure Firefox manually.
- Firefox path: Preferences → General → Network Settings → Manual proxy configuration.
- Set proxy host to `127.0.0.1` and port to `8080` for all protocols.
- Burp listens on port 8080 by default in the book's setup.
- Keep a separate browser for target traffic if you want cleaner proxy history.
- Verification: turn Proxy interception on, browse to a site, and confirm requests appear in Burp.
- If traffic is absent, re-check Firefox proxy settings.
- HTTPS interception requires installing Burp's CA certificate separately.
- Tools: Burp Suite Community/Professional; Firefox; ZAP is an alternative proxy.
- Edge case: using Burp's embedded browser skips external-browser proxy configuration.
- Remediation: N/A — assessment environment setup.

## Source: Bug Bounty Bootcamp, Ch. 4
