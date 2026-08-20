# libcurl POST Buffer Read-Out-of-Bounds Pattern

- What it is: A copied POST buffer is treated as a null-terminated C string despite a separate explicit length.
- Relevant libcurl options from the book: `CURLOPT_POSTFIELDS`, `CURLOPT_COPYPOSTFIELDS`, `CURLOPT_POSTFIELDSIZE`.
- Review code that duplicates binary POST data and later assumes a terminating `\0`.
- Missing null termination can make a copy/read continue past the intended memory region.
- Embedded null bytes can also truncate data unexpectedly.
- Check whether the duplicated pointer/length is updated consistently after copying.
- False positive: current patched libcurl versions should not reproduce the historical flaw.
- Edge case: binary payload handling differs from ordinary C-string handling.
- Remediation: use explicit lengths consistently and update pointers to the copied buffer.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 13
