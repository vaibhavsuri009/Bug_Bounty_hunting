# Quasi-Cash Reward Loop

- What it is: Rewards or cashback can be abused when users can transact with entities they also control and recycle funds at lower fees than the reward rate.
- Where to look / how to identify it:
  - Map payment intermediaries, merchant accounts, refunds, cashback, points, and cash-equivalent instruments.
- Exploitation / test pattern:
  - Use only test/sandbox accounts to model circular transactions and compare fee versus reward economics.
- Tools + exact CLI syntax (if mentioned):
  - Payment sandbox and transaction modeling.
- Common false-positive / WAF / edge-case notes:
  - Self-payments may already be prohibited by processor rules; validate actual platform controls.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Detect related-party transactions, exclude quasi-cash categories, and cap/reverse rewards.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 18
