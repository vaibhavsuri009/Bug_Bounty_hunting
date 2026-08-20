# Legacy API Version OTP Rate-Limit Bypass

- What it is: A retired API version may omit OTP attempt limits used by the current version.
- Where to look / how to identify it:
  - Identify current OTP endpoint/version; swap older versions; compare failure behavior and attempt limits using your own reset flow; book lab: `/v3` limited attempts while `/v2` did not.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Different error text alone is not proof; OTP expiry may mask behavior.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Centralize OTP controls across every version.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
