# API Rate-Limit Enforcement Test

- What it is: The API fails to enforce an expected request quota or throttling control.
- Establish a normal baseline and identify documented rate limits/headers.
- Send a controlled burst of requests within authorized thresholds.
- A functioning limit commonly returns HTTP `429 Too Many Requests`.
- Record whether the limit is keyed to account, token, client, route, or IP.
- After being limited, test benign variations such as parameter/client changes only if allowed.
- False positive: a generous limit is not the same as no limit.
- Edge case: distributed gateways can apply inconsistent counters.
- Remediation: enforce centralized quotas with account/token/IP-aware throttling.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
