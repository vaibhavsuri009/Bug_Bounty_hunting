# ImageMagick Delegate Command Injection

- What it is: Historical ImageMagick delegate processing inserted attacker-controlled data into shell commands.
- Prerequisite: authorized testing of an unpatched ImageMagick/ImageTragick path.
- The book shows a delegate command where `%M` reaches `wget` unsafely.
```text
https://example.com";|id "
```
- Use only a benign command such as `id` when reproducing in a lab/authorized target.
- Prefer validating the payload first on your own server.
- False positive: patched ImageMagick versions/policy.xml configurations block this class.
- Edge case: the triggering input can be inside MVG/SVG even when the filename ends in `.jpg`.
- Remediation: patch ImageMagick and disable risky delegates/coders with restrictive policy.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
