# Referer-Based Open Redirect

- **What it is:** A redirect uses the request `Referer` as the destination without sufficient validation.
- **Where to look:** Pages that redirect after an action but have no obvious redirect parameter.
- Host a simple page on a domain you control that links to the target workflow.
- Visit your page first so the browser sets your origin as the target request's `Referer`.
- Complete the target action and observe whether the application redirects back to your site.

```html
<html>
  <a href="https://example.com/login">Test login</a>
</html>
```

- Confirm with your own test account and authorized domain only.
- **False positives / edge cases:** Browser referrer policy may suppress or truncate the header.
- **Remediation:** Never trust `Referer` as a redirect destination; use fixed server-side destinations or a strict allowlist.

## Source: Bug Bounty Bootcamp, Ch. 7
