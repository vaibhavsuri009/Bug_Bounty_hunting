# Managed-Language Native Extension Overflow Hunting

- What it is: PHP/Python code may expose memory corruption through native extensions written in C.
- Do not stop memory-bug review because the top-level application uses a managed language.
- Identify native modules/extensions handling variable-length network or file data.
- Review counters and sizes stored in fixed-width integers.
- The book's PHP FTP example overflowed an unsigned 32-bit size after extremely large input.
- Native modules using `memcpy()` or manual buffers are higher-value review targets.
- False positive: a crash alone does not prove attacker-controlled memory corruption or code execution.
- Edge case: architecture (32-bit vs 64-bit) changes integer and allocation limits.
- Remediation: use checked arithmetic, bounded copies, and patched native libraries.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 13
