# Burp Intruder Request Fuzzing

- What it is: Automate repeated requests while replacing selected request fields with payload values.
- Capture a representative request in Burp Proxy.
- Right-click → **Send to intruder**.
- Confirm target host and port.
- In **Positions**, mark only the request segment to mutate.
- In **Payloads**, load candidate values such as IDs, attack strings, or test inputs.
- Start the attack and review each response.
- Compare status codes, response lengths, and body differences for anomalies.
- Example login pattern: keep `username` fixed and vary the `password` field.
- Example access-control pattern: vary numeric object IDs in a request.
- Burp Community includes a limited/slower Intruder implementation.
- False-positive trap: response differences may be caused by rate limits, session expiry, or dynamic content; verify interesting cases manually.
- Remediation: N/A — testing technique; fix the underlying validation/authentication flaw found.

## Source: Bug Bounty Bootcamp, Ch. 4
