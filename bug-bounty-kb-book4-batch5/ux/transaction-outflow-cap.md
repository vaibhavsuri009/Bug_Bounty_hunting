# Transaction Outflow Cap

- What it is: User-configurable transaction limits reduce blast radius if an account is compromised.
- Where to look / how to identify it:
  - Review high-value wallets, payments, transfers, API keys, or other irreversible operations.
- Exploitation / test pattern:
  - Validate in a sandbox that configured caps are enforced server-side across all transaction paths.
- Tools + exact CLI syntax (if mentioned):
  - Business-logic tests.
- Common false-positive / WAF / edge-case notes:
  - Client-only limits are bypassable and do not provide real protection.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Enforce caps centrally and add step-up verification for unusually large outflows.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 23
