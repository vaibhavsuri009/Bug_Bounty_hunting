# ImageMagick Extension-Only Upload Bypass

- What it is: The application trusts a filename extension, while ImageMagick detects the real format from file contents.
- Look for image-processing uploads backed by ImageMagick.
- Create a harmless test file in an alternate supported format such as SVG/MVG.
- Rename it with an allowed image extension such as `.jpg`.
- If ImageMagick still parses it as SVG/MVG, extension-only validation is ineffective.
- This was relevant to historical ImageTragick delegate-command vulnerabilities.
- False positive: format sniffing itself is expected; exploitation requires a vulnerable processing path.
- Edge case: patched ImageMagick policy files can block dangerous coders/delegates.
- Remediation: patch ImageMagick and validate both decoded media type and processing policy.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
