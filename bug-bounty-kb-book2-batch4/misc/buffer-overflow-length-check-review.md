# Buffer Overflow Length-Check Review

- What it is: Data larger than its allocated buffer is written into adjacent memory.
- Focus code review on C/C++ memory-copy and allocation paths.
- High-signal functions mentioned in the book: `strcpy()`, `memcpy()`, `malloc()`, `calloc()`.
- Trace attacker-controlled source length to the destination buffer size.
```c
char dest[16];
strcpy(dest, src);
```
- Verify room for the full data plus the terminating null byte.
- Hardware/compiler memory alignment can hide small mistakes, so do not assume one test proves safety.
- False positive: an unsafe-looking function is not exploitable if strict bounds are enforced before the copy.
- Edge case: managed-language applications can still inherit memory bugs from native C/C++ extensions.
- Remediation: enforce bounds before every copy and prefer size-safe APIs.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 13
