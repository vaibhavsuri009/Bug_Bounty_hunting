# Simultaneous Requests with `curl`

- **What it is:** Firing identical state-changing requests at nearly the same time can expose race windows between validation and state update.
- **Where to look:** A captured request for an operation that should be allowed once but not multiple times.
- Copy the legitimate request as a `curl` command from Burp.
- Duplicate the command several times in a Unix shell.
- Separate commands with `&` so they run concurrently in the background.

```bash
curl <request> & curl <request> & curl <request> & curl <request>
```

- Send enough simultaneous requests to increase the chance of overlapping server execution.
- Repeat the test if the first run does not hit the race window.
- Check the resulting balance/count/state, not only HTTP status codes.
- **False positives / edge cases:** Retries, asynchronous queues, or eventual consistency can create duplicate-looking responses without violating the final business rule.
- **Remediation:** Use atomic transactions/locks around the validation and update sequence.

## Source: Bug Bounty Bootcamp, Ch. 12
