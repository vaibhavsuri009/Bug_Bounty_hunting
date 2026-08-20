# Cookie-Based Access-Control Bypass

- **What it is:** The server trusts a predictable client cookie such as admin=1 to decide whether a user is privileged.
- **Where to look:** Requests to admin or privileged routes where cookies, headers, or parameters appear to encode role or authorization state.
- **Test / exploitation:**
  - Capture the request made by a privileged workflow or inspect client-side code for role markers.
  - Look for simple authorization values such as admin=0/1, role=user/admin, or similar flags.
  - Modify only the authorization marker while keeping your own valid session.
  - Replay the request and verify whether privileged content/actions become available.
  - Confirm server-side authorization is actually absent rather than a UI-only change.
- **False positives / edge cases:**
  - Changing a client-side display without gaining server-side access is not an authorization bypass.
- **Remediation:** Store authorization state server-side and enforce permissions independently of client-controlled values.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 17
