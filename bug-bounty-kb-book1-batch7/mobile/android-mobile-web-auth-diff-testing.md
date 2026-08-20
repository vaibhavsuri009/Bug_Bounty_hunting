# Android: Compare Mobile vs Web Authorization

- **What it is:** Test whether mobile API endpoints enforce weaker authentication/authorization than the web application.
- **Where to look:** Sensitive actions captured from mobile traffic that use endpoints absent from the web flow.
- **Method:** Intercept mobile actions in Burp, map request parameters/tokens, then compare equivalent web behavior.
- **Test cases:** IDOR, broken authentication, token reuse, long sessions, and tokens surviving logout/password changes.
- **Why it works:** Developers may trust traffic from the mobile client or apply different controls.
- **False positives:** Different endpoints may intentionally expose different public data; verify authorization expectations.
- **Remediation:** Apply consistent server-side access control across web, mobile, and API interfaces.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
