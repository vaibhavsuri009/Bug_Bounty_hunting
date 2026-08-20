# CSRF Testing on API Endpoints

- What it is: Browser-reachable API endpoints can be CSRF targets when they rely on ambient cookies and accept cross-origin form requests.
- Where to look: Mobile/web APIs that modify profiles, settings, zones, connections, or other user state.
- Capture API calls during normal application workflows with an intercepting proxy.
- Identify state-changing endpoints using cookie-based authentication.
- Recreate the request as a cross-origin HTML form when its body is form-compatible.
- Generic pattern:
```html
<form action="https://target.example/api/v2/resource" method="POST">
<input type="hidden" name="value" value="test">
</form>
```
- Test with your own account and verify whether the API accepts the request without a valid CSRF control.
- Edge case: APIs using explicit authorization headers rather than ambient browser credentials may not be CSRF-exploitable.
- Remediation: Apply CSRF protections consistently to browser-accessible API endpoints, not only HTML routes.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 4
