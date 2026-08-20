# CSRF Auto-Submitting HTML Form PoC

- **What it is:** Confirms whether a foreign origin can perform an authenticated state-changing request.
- **Where to look:** Endpoints with missing or bypassable CSRF protection.
- Reproduce the legitimate request as an HTML form and auto-submit it in a browser already logged into your test account.

```html
<form method="POST" action="https://example.com/password_change" id="csrf-form">
  <input name="new_password" value="test-value">
</form>
<script>document.getElementById('csrf-form').submit();</script>
```

- Verify the action succeeded in your own account.
- The test proves cross-site request acceptance; it does not require reading the response.
- **False positives / edge cases:** SameSite cookies may prevent the authenticated cookie from being sent cross-site.
- **Remediation:** Use per-session/action anti-CSRF tokens plus SameSite cookies and origin validation.

## Source: Bug Bounty Bootcamp, Ch. 9
