# API Excessive Data Exposure

- What it is: An endpoint returns fields or records beyond what the consumer needs or is authorized to see.
- Make legitimate requests for your own resources and inspect the complete raw response.
- Compare what the UI uses with everything the API returns.
- Look for hidden admin IDs, roles, emails, MFA state, internal references, and unrelated users.
- Test multiple endpoints because overexposure may occur only in one response variant.
- Do not rely on the frontend filtering sensitive fields from display.
- False positive: extra non-sensitive metadata may be intentional and harmless.
- Edge case: nested objects frequently contain the most sensitive surplus fields.
- Remediation: perform server-side response filtering and return only required fields.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
