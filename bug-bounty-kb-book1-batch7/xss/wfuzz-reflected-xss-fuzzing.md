# Wfuzz: Reflected XSS Fuzzing

- **What it is:** Insert an XSS payload list into reflected input points and locate responses that contain the payload.
- **Where to look:** Search fields, URL parameters, form fields, and other reflected values.
- **Filter:** Wfuzz `--filter "content~FUZZ"` can return responses containing the injected string.
- **Method:** Fuzz → locate reflection → manually determine HTML/JS context → craft a safe executable PoC.
- **False positives:** Reflection alone is not XSS if the output is correctly encoded or in a non-executable context.
- **Edge case:** Redirect-based XSS payload lists can also be tracked with verbose redirect output.
- **Remediation:** Contextually encode output and apply appropriate input handling/CSP defense-in-depth.

```bash
wfuzz -w xss.txt --filter "content~FUZZ" 'http://example.com/get_user?user_id=FUZZ'
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
