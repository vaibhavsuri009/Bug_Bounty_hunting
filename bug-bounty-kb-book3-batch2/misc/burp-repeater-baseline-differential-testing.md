# Burp Repeater Baseline Differential Testing

- What it is: Repeater lets you change one request component at a time and compare server behavior.
- Capture a legitimate API request in Proxy and send it to Repeater.
- Send the request unchanged to establish a baseline.
- Modify one parameter, header, method, body field, or identifier.
- Compare status code, body, headers, length, and timing with the baseline.
- Use this workflow before automating with Intruder so you know what a meaningful response looks like.
- False positive: dynamic content can create differences unrelated to the modified input.
- Edge case: expiring tokens/nonces may require refreshing the baseline frequently.
- Remediation note: validate and authorize every client-controlled field server-side.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
