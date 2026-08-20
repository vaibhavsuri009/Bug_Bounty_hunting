# Wfuzz: SQL Injection Fuzzing

- **What it is:** Send a SQLi payload list through an input point and detect response anomalies.
- **Where to look:** Query/body parameters that influence database-backed operations.
- **POST body:** Wfuzz `-d` specifies request body data.
- **Detection:** Compare response time, status, and length; time-delay payloads should create repeatable latency if executed.
- **Validation:** Replay promising payloads manually and prove database influence without destructive actions.
- **False positives:** Network jitter and backend load can imitate time-based SQLi; use repeated controls.
- **Remediation:** Use parameterized queries/prepared statements and least-privilege DB accounts.

```bash
wfuzz -w sqli.txt -d 'user_id=FUZZ' http://example.com/get_user
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
