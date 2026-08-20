# API Mass Assignment via Hidden Properties

- What it is: The API automatically binds extra request properties to backend objects.
- Capture a legitimate account create/update request.
- Find additional object properties in documentation, responses, frontend code, or schemas.
- Add one candidate property at a time.
```json
{"User":"test","Password":"Test123!","isAdmin":true}
```
- Verify whether the server persists the unauthorized property.
- False positive: echoing the extra field does not prove it affected backend state.
- Edge case: blind mass assignment may require observing a secondary effect.
- Remediation: explicitly allowlist writable properties for each operation.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
