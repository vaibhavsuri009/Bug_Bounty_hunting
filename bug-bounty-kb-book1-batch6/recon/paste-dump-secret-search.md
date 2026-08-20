# Paste Dump Secret Search

- **What it is:** Public paste/code-sharing services may expose source, configuration, logs, API keys, or passwords associated with the target.
- **Where to look:** Pastebin, GitHub gists, and similar public paste services using company domains, emails, or project keywords.
- **Test / exploitation:**
  - Search using organization-specific keywords, domains, and email identifiers.
  - Review returned public pastes for configuration and credential material.
  - Validate that any discovered credential belongs to the in-scope organization and is still active before reporting.
  - Avoid accessing unrelated third-party data.
- **Tools / syntax:**
```text
./scrape.sh -g KEYWORD
```
- **False positives / edge cases:**
  - Public pastes can contain false, old, or unrelated credentials.
- **Remediation:** Avoid using public paste sites for secrets and rotate exposed credentials.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 21
