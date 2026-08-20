# Proxy Postman Through Burp Suite

- What it is: Postman builds API requests while Burp intercepts them for deeper manipulation.
- Open Postman Settings → Proxy.
- Enable a custom proxy.
- Set proxy server to `127.0.0.1` and port `8080`.
- Disable Postman SSL certificate verification for this testing setup.
- In Burp, turn Proxy interception on and send a Postman request.
- Confirm that the request appears in Burp before continuing.
- False positive: TLS/proxy errors can originate from local tooling configuration.
- Edge case: keep the proxy configured but toggle Burp interception as needed.
- Remediation note: testing proxy configuration should never be deployed to production clients.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
