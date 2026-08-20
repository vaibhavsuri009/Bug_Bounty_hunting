# Code Review: Developer Comments and Debug Endpoints

- **What it is:** Mine comments and hidden development functionality for unfinished controls, credentials, and undocumented endpoints.
- **Where to look:** Comments, debug flags, dev URLs, configuration references, deprecated routes, and code marked incomplete.
- **Keywords mentioned:** `todo`, `fix`, `completed`, `config`, `setup`, `removed`, plus `http`, `https`, `ftp`, `dev`.
- **Config extensions:** `.conf`, `.env`, `.cnf`, `.cfg`, `.cf`, `.ini`, `.sys`, `.plist`.
- **Example clue:** A comment stating CSRF protection is not implemented can directly focus testing.
- **False positives:** Comments can be stale; verify the referenced endpoint/control in the live code path.
- **Remediation:** Remove debug functionality from production and prevent secrets/security TODOs from shipping.

```bash
grep -RniE 'todo|fix|debug|dev\.|config|setup|removed|https?://|ftp://' .
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
