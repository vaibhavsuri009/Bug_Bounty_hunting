# Mass Assignment via Registration Admin Flag

- What it is: A registration endpoint may bind extra client-supplied model fields such as an admin flag.
- Where to look / how to identify it:
  - Capture a normal registration JSON body and add one likely privileged field, e.g. `"admin":true`; register only a controlled test account and verify persisted role.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Echoing the field does not prove privilege changed.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Allowlist writable registration properties and ignore privileged server-owned fields.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 11
