# IDOR Authorization Automation with Burp

- **What it is:** Repetitive IDOR testing can be automated by replaying requests with lower-privilege identities and altered object references.
- **Where to look:** Large applications with many authenticated endpoints and role combinations.
- Use Burp Intruder to iterate through candidate object IDs when permitted by program rules.
- Compare response status, length, and content for authorization differences.
- Burp extensions mentioned in the book:
  - Autorize: replays higher-privilege requests using lower-privilege credentials.
  - Auto Repeater: automates substitutions in cookies, headers, and parameters.
  - AuthMatrix: tests authorization behavior across multiple identities/roles.
- Install extensions from Burp's Extender/BApp Store area.
- Validate every automated finding manually with controlled accounts.
- **False positives / edge cases:** Different response sizes or codes can result from personalization rather than broken authorization.
- **Remediation:** Centralize and test object-level authorization across every role and endpoint.

## Source: Bug Bounty Bootcamp, Ch. 10
