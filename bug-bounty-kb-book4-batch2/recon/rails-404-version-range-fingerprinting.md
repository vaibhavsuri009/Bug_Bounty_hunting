# Rails 404 Version-Range Fingerprinting

- What it is: Ruby on Rails default 404 page changes can be used to narrow the framework release range.
- Where to look / how to identify it:
  - Compare markers such as historical HTML attributes, whitespace changes, and namespaced error-page CSS.
- Exploitation / test pattern:
  - Cross-reference observed markers against Rails commit history and official release dates.
- Tools + exact CLI syntax (if mentioned):
  - `git clone https://github.com/rails/rails` then review 404-page history.
- Common false-positive / WAF / edge-case notes:
  - Custom 404 pages break this fingerprinting method.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Replace default framework error pages and keep Rails updated.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
