# 2FA OTP Account-Binding Test

- What it is: An OTP generated during one login flow can be paired with a different username/account.
- Use two controlled accounts and intercept the OTP submission request.
- Add or modify the username/login field while preserving the OTP field.
- Verify whether the backend binds the OTP to the original authenticated first factor.
- Test token lifetime, attempt limits, expiry, and reuse.
- The historical GitLab flaw accepted a manipulated `user[login]` parameter in the OTP request.
- False positive: generating an OTP for another username is not enough if the attacker cannot validate it.
- Edge case: 30-second TOTP windows make race/brute-force claims sensitive to attempt limits.
- Remediation: bind OTP verification to the server-side first-factor session and exact account.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
