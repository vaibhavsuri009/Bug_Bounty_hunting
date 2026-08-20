# SQL String Concatenation Signal

- What it is: SQL injection commonly appears when attacker-controlled input is concatenated directly into a query string.
- Where to look / how to identify it:
  - Review code or request behavior where identifiers, usernames, filters, or search data flow directly into SQL statements.
- Exploitation / test pattern:
  - Use harmless syntax-error probes on controlled data to confirm whether input reaches the SQL parser.
- Tools + exact CLI syntax (if mentioned):
  - Source review plus safe request replay.
- Common false-positive / WAF / edge-case notes:
  - A SQL error does not prove arbitrary query execution; confirm safely.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use parameterized queries/prepared statements and avoid string-built SQL.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 13
