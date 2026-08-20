# GraphQL: Recon When Introspection Is Disabled

- **What it is:** Recover likely GraphQL structure from observable application behavior when normal introspection is unavailable.
- **Where to look:** Client queries, JavaScript, mobile traffic, error messages, public docs, and known operations.
- **Tool mentioned:** Clairvoyance helps gain insight into GraphQL structure when introspection is disabled.
- **Workflow:** Capture legitimate queries → collect type/field names → test adjacent fields/operations → validate authorization.
- **False positives:** Guessed fields can produce generic errors that reveal little; distinguish parsing vs authorization failures.
- **Edge case:** GraphQL Playground/ZAP add-ons can assist where introspection is available.
- **Remediation:** Disabling introspection reduces recon but does not replace authorization controls.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
