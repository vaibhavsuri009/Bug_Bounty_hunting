# Google Dorks for API Secrets and Documentation

- What it is: Advanced search operators uncover indexed API files, docs, directories, and exposed keys.
- Useful operators: `intitle`, `inurl`, `filetype`, and `site`.
- Narrow generic API searches by the target domain or organization name.
- Examples from the book include searches for WordPress user APIs, indexed `api.txt`, API directories, and exposed API-key strings.
- Use GHDB as a source of reusable dork patterns.
- Verify every result belongs to the target and is in scope.
- False positive: indexed pages may be cached, stale, or unrelated mirrors.
- Edge case: search engines can expose secrets that should be reported without attempting privileged use.
- Remediation: remove exposed secrets and prevent sensitive files from being publicly indexed.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 6
