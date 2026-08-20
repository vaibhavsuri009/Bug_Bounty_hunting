# Arbitrary File Write to SSH `authorized_keys`

- What it is: A file-write primitive becomes remote shell access if it can overwrite a privileged user's SSH authorized keys.
- Prerequisite: explicit authorization to test high-impact file-write escalation.
- The book's chain targets:
```text
/root/.ssh/authorized_keys
```
- Write only a dedicated test public key and remove it immediately after validation.
- Confirm access with a harmless command such as `id`.
- This chain requires both filesystem write permission and an exposed/reachable SSH service.
- False positive: writing the file is insufficient if SSH is disabled or another configuration prevents key authentication.
- Edge case: testing this may exceed normal bug-bounty rules; obtain permission first.
- Remediation: constrain write paths, run services as non-root, and harden SSH/file permissions.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
