# API Response-Time Side-Channel Enumeration

- What it is: Timing differences reveal whether a supposedly nonexistent resource actually exists.
- Establish a baseline using multiple known-invalid resource IDs.
- Measure known-valid IDs to establish the alternate timing distribution.
- Compare a larger candidate set against both baselines.
- The book illustrates this with `X-Response-Time` values such as ~25 ms vs ~510 ms.
- Use repeated samples to reduce network-noise errors.
- False positive: caching, backend load, and routing can create timing outliers.
- Edge case: explicit timing headers make the side channel easier but are not required.
- Remediation: normalize code paths/errors and avoid unnecessary detailed timing headers.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
