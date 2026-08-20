# Self-XSS Chaining with Login/Logout CSRF

- What it is: A self-XSS becomes cross-user impact only if another flaw can force the victim into the attacker's state.
- First verify the XSS affects only the submitting account/session.
- Then look for login or logout CSRF that can move a target into an attacker-controlled account.
- The conceptual chain is: force session state -> victim renders attacker-stored payload -> JavaScript executes.
- Do not claim severity based on self-XSS alone.
- Verify each prerequisite separately before presenting the chain.
- False positive: if authentication requires an unforgeable CSRF token, the chain may not be possible.
- Edge case: SameSite cookies and modern login protections often block cross-site session forcing.
- Keep proof-of-concept actions benign and reversible.
- Remediation: fix the XSS and add robust CSRF protections to authentication state transitions.
- Check whether the target must manually paste/execute code; if so, it remains self-XSS rather than a practical cross-user chain.
- Record the exact user interaction required so the report does not overstate exploitability.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
