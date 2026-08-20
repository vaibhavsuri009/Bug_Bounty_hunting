# API Authorization Testing Checklist

- What it is: Authorization testing asks how resources are identified and whether another user or role can access or modify them.
- Where to look / how to identify it:
  - Use A-B tests for object access and A-B-A tests for state-changing functions with controlled accounts.
- Exploitation / test pattern:
  - Test the same operation across roles and methods, then verify server-side effects.
- Tools + exact CLI syntax (if mentioned):
  - Postman collection token swaps and Burp Match and Replace can scale controlled tests.
- Common false-positive / WAF / edge-case notes:
  - Public/shared resources can create false positives; define the expected access boundary first.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Apply BOLA and BFLA controls server-side for every resource and action.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. A
