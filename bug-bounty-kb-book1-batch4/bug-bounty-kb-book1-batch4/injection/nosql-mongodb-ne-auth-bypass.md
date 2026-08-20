# MongoDB `$ne` Authentication Bypass

- **What it is:** Unvalidated structured input can inject MongoDB query operators instead of a literal password value.
- **Where to look:** JSON/form login endpoints backed by MongoDB or similar document databases.
- Identify whether input reaches a query shaped like `Users.find({username:$u,password:$p})`.
- Test operator-style input rather than a scalar value.

```text
username=admin
password={$ne:""}
```

- `$ne` means "not equal"; the condition can match an account whose password is not blank.
- Confirm only against a controlled test account or authorized target.
- **False positives / edge cases:** Framework parsing may treat the payload as a plain string instead of an object/operator.
- **Remediation:** Validate input types and construct queries using trusted operators with untrusted values only as data.

## Source: Bug Bounty Bootcamp, Ch. 11
