# GraphQL Variable Command-Injection Fuzzing

- What it is: GraphQL variables can reach backend commands or libraries, making them potential injection points.
- Where to look / how to identify it:
  - Prioritize mutation variables that accept host, path, filename, URL, or other backend-facing input.
- Exploitation / test pattern:
  - Fuzz one variable at a time with harmless command separators and benign commands in an authorized lab, then compare responses.
- Tools + exact CLI syntax (if mentioned):
  - Burp Intruder cluster-bomb approach can pair separators with harmless commands such as `whoami`.
- Common false-positive / WAF / edge-case notes:
  - A parser error is not proof of OS execution; require deterministic evidence from a harmless command.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Avoid shell construction from user input; use safe APIs and strict allowlists.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
