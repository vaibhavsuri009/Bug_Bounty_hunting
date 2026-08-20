# HTTP Method Enumeration with OPTIONS

- What it is: `OPTIONS` can reveal which HTTP methods an API endpoint claims to support.
- Send an `OPTIONS` request to an API endpoint.
- Inspect the response for allowed methods.
- Compare documented methods with what the server actually accepts.
- Pay special attention to `PUT`, `PATCH`, `DELETE`, `TRACE`, and `CONNECT`.
- Follow up with harmless requests using unexpected methods on resources you control.
- False positive: an `Allow` header may be generic and not reflect route-level authorization.
- Edge case: gateways and backend services can disagree about method handling.
- Remediation: disable unnecessary methods and enforce authorization per method/action.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 1
