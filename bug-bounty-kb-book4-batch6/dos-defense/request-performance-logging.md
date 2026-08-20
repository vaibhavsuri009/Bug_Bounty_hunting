# DoS-Oriented Request Performance Logging

- What it is: Server-side DoS attempts can be difficult to detect unless requests and asynchronous jobs are logged with resource/timing data.
- Where to look / how to identify it:
  - Record endpoint, actor, request rate, response time, queue time, errors, and async-job duration.
- Exploitation / test pattern:
  - Use logs to establish normal baselines and investigate repeated expensive operations.
- Tools + exact CLI syntax (if mentioned):
  - Application metrics/APM/SIEM.
- Common false-positive / WAF / edge-case notes:
  - High latency can come from normal load or dependencies rather than an attack.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Build endpoint-level performance telemetry and alert on abnormal resource consumption.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 32
