# CSRF Token Removal and Tampering Test

- What it is: A token can exist in requests yet be optional, weakly validated, or ignored.
- Where to look: State-changing requests containing fields/headers resembling `csrf`, `X-CSRF-TOKEN`, `rt`, `form-id`, or similar values.
- Capture a legitimate request containing the token.
- Replay it unchanged to establish a baseline.
- Remove the token completely and resend.
- Send the token with an empty value.
- Replace the token with a random value or a token from another test session.
- Confirm whether the state-changing action still succeeds in any invalid-token case.
- Also test whether validation is conditional only when the parameter is present.
- Compare both HTTP status and the actual resulting account state after each replay.
- False-positive trap: A token name alone proves nothing; the server must reject missing/invalid tokens consistently.
- Remediation: Require and validate a strong user/session-bound token on every protected state-changing request.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 4
