# Blind RCE via Time Delay

- **What it is:** Code executes without returning command output, so execution is inferred from a controlled delay.
- **Where to look:** Suspected command/code injection points that return generic or unchanged responses.
- **Test / exploitation:**
  - Measure several baseline response times.
  - Inject a harmless sleep command for a fixed duration.
  - Repeat the delayed request and compare against baseline.
  - Reduce or vary the delay to confirm correlation with the supplied value.
  - Use an out-of-band callback if timing remains noisy.
- **Tools / syntax:**
```text
sleep 5
| sleep 10;
$(sleep 10)
```
- **False positives / edge cases:**
  - Backend slowness, queues, and network jitter can create false timing signals.
- **Remediation:** Eliminate unsafe execution paths and validate/parameterize any unavoidable command arguments.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
