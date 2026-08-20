# API Trust-Assumption Testing

- What it is: Business logic relies on consumers obeying documentation or using the API only through the intended UI.
- Search documentation for phrases such as "only use X for Y," "do not do X," or "only admins should."
- Intercept the underlying API request with Burp/Postman.
- Modify parameters/actions that the UI normally prevents.
- Example from the book: change a client-controlled `MFA=true` field to `MFA=false` and verify server behavior on your own account.
- Focus on assumptions that are not backed by server-side controls.
- False positive: a manipulated parameter may be ignored while the server enforces the real state elsewhere.
- Edge case: partner APIs can expose high-impact trust failures if downstream partners forward privileged requests.
- Remediation: replace trust assumptions with explicit server-side authorization and validation.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
