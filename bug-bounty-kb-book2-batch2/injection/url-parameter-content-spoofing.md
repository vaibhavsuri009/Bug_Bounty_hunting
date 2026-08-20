# URL Parameter Content Spoofing

- What it is: A controllable URL parameter is decoded and displayed as trusted-looking plaintext.
- Look for parameters tied to errors, notices, status messages, or login feedback.
- Change the parameter from its expected value to a unique benign marker.
```text
?error=access_denied
?error=TEST-MESSAGE
```
- If the marker is rendered in a privileged-looking area, test URI-encoded spaces/punctuation.
- Demonstrate impact with clearly non-deceptive test text rather than real phishing content.
- Content spoofing differs from HTML injection: tags may be stripped while plaintext still appears.
- False positive: user-controlled text shown in an explicitly user-generated area may be intended behavior.
- Edge case: the issue is usually low severity unless placement creates credible trust confusion.
- Remediation: map parameters to fixed server-side messages instead of rendering arbitrary parameter values.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 5
