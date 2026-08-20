# PHP Serialized Property Tampering

- Unsigned/unencrypted PHP serialized objects can expose security-relevant properties to client-side modification.
- Look for roles, usernames, status flags, file paths, or control-flow values inside serialized objects.
- Example vulnerable property change:
```text
status = "not admin"  ->  status = "admin"
```
- Serialized form must keep correct string-length markers:
```text
s:6:"status";s:5:"admin";
```
- Intercept the request, replace the original serialized object, and observe whether authorization changes.
- Test with a separate low-privilege account and a harmless privilege-dependent action.
- False-positive trap: applications may sign/MAC the serialized blob or independently enforce server-side authorization.
- Remediation: never trust authorization data stored in client-controlled serialized objects; enforce permissions server-side.
## Source: Bug Bounty Bootcamp, Ch. 14
