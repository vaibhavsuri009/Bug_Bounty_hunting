# API BOLA Object-ID Swap

- What it is: Broken Object Level Authorization lets one user access another user's API object.
- Identify object IDs in paths, query parameters, and bodies.
- Capture a request for an object owned by account A.
- While authenticated as account B, replace B's object ID with A's.
```text
GET /api/resource/1
GET /api/resource/3
```
- Successful unauthorized access confirms BOLA; predictable IDs alone do not.
- False positive: objects may intentionally be shared or public.
- Edge case: IDs can be names, UUIDs, company names, or numeric values.
- Remediation: enforce object ownership/authorization on every request.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
