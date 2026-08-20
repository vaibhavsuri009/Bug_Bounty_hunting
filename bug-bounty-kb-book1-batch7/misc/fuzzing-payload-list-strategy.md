# Fuzzing: Payload List Strategy

- **What it is:** Choose payload sets matched to the injection point and vulnerability being tested.
- **Sources recommended:** SecLists, Big List of Naughty Strings, and FuzzDB.
- **Method:** Use vulnerability-specific lists for XSS/SQLi/XXE/etc., plus targeted enumeration lists for paths or IDs.
- **Random fuzzing:** The book also suggests very long values, unusual encodings, and special characters such as newlines/line feeds.
- **Generation:** Bash loops or `/dev/random` can help create random test data.
- **False positives:** Garbage input causing a generic 500 is only a lead; reproduce and determine security impact.
- **Remediation:** Handle malformed input safely and consistently without leaking internals.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
