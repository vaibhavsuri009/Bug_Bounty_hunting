# Live Offensive Testing Safety

- What it is: Some offensive techniques can disrupt users or compromise systems even when the tester has general permission.
- Where to look / how to identify it:
  - Before testing high-impact techniques, identify potential destructive side effects and confirm specific authorization.
- Exploitation / test pattern:
  - Prefer local/sandbox reproduction for DoS, command execution, destructive BFLA, and supply-chain scenarios.
- Tools + exact CLI syntax (if mentioned):
  - Written scope and test plan.
- Common false-positive / WAF / edge-case notes:
  - General bug-bounty scope does not imply permission for disruptive testing.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Define prohibited actions, staging targets, stop conditions, and communication channels.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 19
