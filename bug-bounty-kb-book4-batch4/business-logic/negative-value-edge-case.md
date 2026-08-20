# Negative Numeric Edge Case

- What it is: Business logic may accept negative amounts where only positive values make sense, inverting credit/debit behavior.
- Where to look / how to identify it:
  - Look at prices, transfers, invoices, quantities, credits, refunds, and balance adjustments.
- Exploitation / test pattern:
  - Test `0`, minimum, maximum, and small negative values only in controlled environments.
- Tools + exact CLI syntax (if mentioned):
  - API request editing.
- Common false-positive / WAF / edge-case notes:
  - Negative values can be valid in accounting contexts; confirm expected domain rules.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use server-side range validation and domain-specific numeric types.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 18
