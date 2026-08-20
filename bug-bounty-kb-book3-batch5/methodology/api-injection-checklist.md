# API Injection Testing Checklist

- What it is: Injection testing begins with requests that accept user input and can reach a browser, database, interpreter, or operating system.
- Where to look / how to identify it:
  - Prioritize query strings, headers, tokens, keys, and POST/PUT body parameters.
- Exploitation / test pattern:
  - Confirm suspicious behavior with harmless proof and technology-specific follow-up.
- Tools + exact CLI syntax (if mentioned):
  - Book categories include XSS/XAS, SQL/NoSQL injection, and OS command injection.
- Common false-positive / WAF / edge-case notes:
  - Verbose errors are clues, not proof; avoid destructive payloads on live targets.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use parameterized queries, safe process APIs, output encoding, and strict validation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. A
