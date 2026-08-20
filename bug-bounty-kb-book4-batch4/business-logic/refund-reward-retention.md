# Refund + Reward Retention Check

- What it is: Rewards systems may fail to reverse benefits after a purchase is refunded or reversed.
- Where to look / how to identify it:
  - Test a controlled purchase/refund cycle and inspect whether points, cashback, or credits are reclaimed.
- Exploitation / test pattern:
  - Use low-value sandbox transactions only.
- Tools + exact CLI syntax (if mentioned):
  - Payment/reward test environment.
- Common false-positive / WAF / edge-case notes:
  - Delayed reward reconciliation can appear vulnerable before asynchronous reversal completes.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Tie reward state to final settlement and automatically reverse rewards on refund/chargeback.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 18
