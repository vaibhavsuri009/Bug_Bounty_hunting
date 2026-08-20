# Multiple Database Attack Surface

- What it is: Modern applications may use SQL, NoSQL, search databases, and specialized stores simultaneously.
- Where to look / how to identify it:
  - Identify database technologies from headers, errors, source code, dependencies, and data behavior.
- Exploitation / test pattern:
  - Do not stop after confirming one secure query layer; map all data stores involved in the same application.
- Tools + exact CLI syntax (if mentioned):
  - Recon notes + source/error analysis.
- Common false-positive / WAF / edge-case notes:
  - Database identification can be uncertain when services are abstracted behind APIs.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use safe query APIs for every datastore and apply least privilege independently to each database.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
