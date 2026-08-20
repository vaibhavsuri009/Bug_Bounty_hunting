# Code Review: One Input, Multiple Vulnerable Sinks

- **What it is:** A single user-controlled value can create multiple bugs when reused in different contexts.
- **Source example:** A URL path is concatenated into a shell command and later echoed into HTML.
- **Method:** For every input variable, enumerate all uses instead of stopping after finding the first issue.
- **Command sink:** Input reaching `system()` can become command injection.
- **HTML sink:** The same value reflected without output encoding can become reflected XSS.
- **False positives:** Each sink has its own parsing/encoding context; test separately.
- **Remediation:** Use safe command APIs and context-specific HTML encoding; avoid raw reuse of attacker input.

```text
download_file -> parse_url -> system(command)   # command injection
              \-> HTML output       # reflected XSS
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
