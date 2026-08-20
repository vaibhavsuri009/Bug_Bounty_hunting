# Address Search Excessive Data Exposure

- What it is: An address lookup can expose unrelated current or historical occupants when the API returns every matching record.
- Where to look / how to identify it:
  - Use controlled addresses/test records and compare the requested data with the full response.
- Exploitation / test pattern:
  - Flag extra names, usernames, email addresses, phone numbers, or account records unrelated to the caller's task.
- Tools + exact CLI syntax (if mentioned):
  - Postman/Collection Runner is sufficient.
- Common false-positive / WAF / edge-case notes:
  - Extra metadata is only a finding when it violates the intended privacy boundary or creates meaningful risk.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Return the minimum necessary fields and authorize access to each returned record.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
