# SQL Injection Automation with sqlmap

- **What it is:** sqlmap automates detection and exploitation of SQL injection after you understand the underlying injection behavior.
- **Where to look:** Parameters already suspected or confirmed to interact unsafely with a SQL database.
- The book recommends understanding manual techniques before automation.
- sqlmap can automate discovery and exploitation of SQL injection vulnerabilities.
- It can be used as a standalone tool or integrated into a testing proxy.
- The book mentions the SQLiPy Burp extension as an integration option.
- No exact sqlmap command-line syntax is provided in this chapter, so none is added here.
- Validate automated results manually before reporting.
- Restrict automation to program scope and permitted testing intensity.
- **False positives / edge cases:** WAF behavior, unstable responses, or parameter reflection can confuse automated detection.
- **Remediation:** Parameterized queries and least-privilege database access remain the primary defenses.

## Source: Bug Bounty Bootcamp, Ch. 11
