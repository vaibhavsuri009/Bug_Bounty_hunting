# BFLA Admin Endpoint Test

- What it is: Broken Function Level Authorization lets a low-privileged user perform higher-privileged API actions.
- Find privileged endpoints in admin documentation or by reverse engineering.
- Authenticate as a low-privileged controlled account.
- Replay admin actions such as create/update/delete against controlled resources.
- Expected secure responses are typically `401` or `403`.
- Also test whether changing HTTP methods exposes privileged functionality.
- False positive: a successful response may perform only a nonprivileged subset of the action.
- Edge case: role boundaries can be lateral (partner-to-partner) as well as vertical.
- Remediation: enforce role/function authorization server-side for every endpoint and method.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
