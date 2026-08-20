# Burp + FoxyProxy Interception Setup

- What it is: Route browser traffic through Burp so requests can be captured and modified.
- Configure a FoxyProxy profile with host `127.0.0.1` and port `8080`.
- Start Burp Suite and turn Proxy interception on.
- Select the Burp proxy profile in the browser and browse to the target.
- The request should pause in Burp before being forwarded to the server.
- Use Forward to continue or send the request to Repeater/Intruder for testing.
- Install Burp’s CA certificate in the browser if HTTPS interception fails.
- False positive: browser connection failures can come from proxy/certificate setup rather than the target.
- Edge case: HSTS/TLS interception requires the Burp CA to be trusted by the testing browser.
- Remediation note: this is tester tooling; production apps should use TLS correctly and consider certificate pinning where appropriate.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
