# `memcpy()` Source/Destination Size Audit

- What it is: `memcpy()` copies exactly the requested byte count without checking destination capacity.
- Search native code for `memcpy(` and identify all three arguments.
```c
memcpy(self->buffer + self->index, s, len);
```
- Determine whether `len` can exceed the remaining size of the destination.
- Work backward to establish whether an attacker controls `s`, `len`, or `self->index`.
- Pay attention to offset arithmetic such as `buffer + index`.
- False positive: a preceding explicit bounds check may make the copy safe.
- Edge case: integer overflow in the bounds calculation can invalidate an apparently correct check.
- Remediation: validate the copy length against remaining destination capacity using overflow-safe arithmetic.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 13
