# Functional + Technical Recon Model

- What it is: Effective reconnaissance combines technical architecture with the application's business purpose, valuable data, users, and revenue-generating functions.
- Where to look / how to identify it:
  - Before deep testing, identify who uses the application, what functions matter most, how the company makes money, and which data is mission-critical.
- Exploitation / test pattern:
  - Record functional priorities beside technical endpoints so later testing can prioritize high-impact features.
- Tools + exact CLI syntax (if mentioned):
  - No specialized tool required; browser, notes, and public business information are sufficient.
- Common false-positive / WAF / edge-case notes:
  - Technical exposure alone does not indicate business impact; understand how the feature is actually used.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain an application inventory that includes data classification, business criticality, and ownership.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 2
