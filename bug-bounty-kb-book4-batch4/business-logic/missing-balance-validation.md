# Missing Balance Validation

- What it is: Financial transfer logic can fail when the server validates the recipient but not whether the sender has sufficient funds.
- Where to look / how to identify it:
  - Map every precondition required for money, credit, inventory, or quota transfers.
- Exploitation / test pattern:
  - Use synthetic balances/test accounts and attempt only harmless boundary cases such as exact-balance and insufficient-balance scenarios.
- Tools + exact CLI syntax (if mentioned):
  - Controlled test accounts; API request replay.
- Common false-positive / WAF / edge-case notes:
  - Database constraints may independently prevent the abuse even if application logic is weak.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Validate all transaction preconditions atomically on the server and database layer.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 18
