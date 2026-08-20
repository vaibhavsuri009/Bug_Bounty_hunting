# Local vs Global Price Validation

- What it is: Systems using local market or pool prices can be manipulated if they assume local demand always reflects an external/global reference price.
- Where to look / how to identify it:
  - Look for trading, rewards, exchange, auction, or liquidity logic that trusts a small internal market.
- Exploitation / test pattern:
  - Use simulation/test data to determine whether one actor can materially move local prices and profit from automated system responses.
- Tools + exact CLI syntax (if mentioned):
  - Offline modeling or test environment only.
- Common false-positive / WAF / edge-case notes:
  - Real markets naturally move; business impact depends on whether the platform bears the loss.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use price bands, external reference feeds, liquidity checks, and anomaly detection.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 18
