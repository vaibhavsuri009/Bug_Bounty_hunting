# CSRF Through a State-Changing GET

- What it is: A GET endpoint changes server-side state and accepts the victim's automatically attached authentication cookies.
- Where to look: Logout/disconnect/delete/toggle/update links that perform an action merely by visiting a URL.
- Capture the action and verify it is triggered by `GET`.
- Embed the action URL as an image source on an attacker-controlled test page:
```html
<img src="https://target.example/account/disconnect">
```
- Load the page while authenticated to the target with your own test account.
- Confirm the browser sends the target cookies and the action occurs without a CSRF token or origin validation.
- Use harmless, reversible actions during validation.
- False-positive trap: A GET that only reads data is not a state-changing CSRF.
- Remediation: Never perform state changes with GET; require CSRF-protected state-changing methods.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 4
