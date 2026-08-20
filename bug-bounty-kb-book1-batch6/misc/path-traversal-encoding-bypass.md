# Path Traversal Encoding Bypass

- **What it is:** Encoded parent-directory sequences bypass filters that reject literal ../ while decoding later in the request pipeline.
- **Where to look:** File/path parameters that block plain traversal strings.
- **Test / exploitation:**
  - Confirm the parameter references a server-side file path.
  - Try plain ../ first to establish behavior.
  - If blocked, try URL-encoded, double-encoded, or partially encoded variants.
  - Repeat enough parent traversals to reach a known nonsensitive file.
  - Confirm actual file retrieval, not only a changed status code.
- **Tools / syntax:**
```text
%2e%2e%2f
%252e%252e%255f
..%2f
```
- **False positives / edge cases:**
  - Different decoding layers may transform payloads differently; errors alone are not proof.
- **Remediation:** Canonicalize once, then enforce the resolved path is inside the intended base directory.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 21
