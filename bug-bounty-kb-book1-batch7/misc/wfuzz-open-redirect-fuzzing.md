# Wfuzz: Open Redirect Fuzzing

- **What it is:** Fuzz redirect parameters with destination/bypass payloads and observe navigation.
- **Where to look:** Parameters such as `redirect`, `next`, `url`, or return locations.
- **Base command:** Place `FUZZ` in the redirect parameter.
- **Detection:** Enable verbose mode and `--follow` to expose redirect behavior and final destinations.
- **Validation:** Confirm a payload sends the browser/client to an attacker-controlled origin.
- **False positives:** Internal-only redirects or blocked schemes may be expected behavior.
- **Remediation:** Enforce exact destination allowlists or server-side relative paths.

```bash
wfuzz -w wordlist.txt -v --follow 'http://example.com?redirect=FUZZ'
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
