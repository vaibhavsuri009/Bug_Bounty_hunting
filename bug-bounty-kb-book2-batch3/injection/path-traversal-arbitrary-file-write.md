# Path Traversal to Arbitrary File Write

- What it is: A write endpoint accepts a user-controlled filesystem path and allows `../` traversal outside the intended directory.
- Look for API parameters named `path`, `file`, `template`, or configuration destinations.
- The book's example changes a normal config path to:
```text
../../../../../../../../../../../../tmp/test.txt
```
- Start by writing a harmless marker to an approved temporary location.
- Confirm the file appears outside the intended application directory.
- False positive: normalized paths may still remain inside a sandbox/chroot.
- Edge case: write permission varies by target directory.
- Remediation: resolve/canonicalize paths, enforce a fixed base directory, and reject traversal.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
