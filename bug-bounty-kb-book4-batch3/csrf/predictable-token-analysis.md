# Predictable CSRF Token Analysis

- What it is: CSRF tokens derived from timestamps, counters, usernames, or other predictable values can sometimes be forged.
- Where to look / how to identify it:
  - Collect a small set of tokens from your own account and compare length, character set, timing, and incremental patterns.
- Exploitation / test pattern:
  - Model the token generator only against your own session and test a predicted value on a harmless action.
- Tools + exact CLI syntax (if mentioned):
  - Spreadsheet/script or Burp Sequencer-style analysis.
- Common false-positive / WAF / edge-case notes:
  - Similarity between a few tokens is not proof of predictability; gather enough samples.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Generate tokens using a cryptographically secure random source with sufficient entropy.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 11
