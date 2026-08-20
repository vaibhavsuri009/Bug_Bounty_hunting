# Code Review: User-Input Taint Tracing

- **What it is:** Follow attacker-controlled data from source to every place it is stored, transformed, and consumed.
- **Sources mentioned:** Request parameters, headers, paths, database entries, file reads, and file uploads.
- **Method:** Mark the source, trace assignments/transformations, then inspect each sink for validation or encoding.
- **Why it matters:** The same input can be safe in one component and exploitable in another.
- **Useful findings:** Stored XSS, SQL injection, XXE, command injection, and open redirects.
- **False positives:** Encoding/validation may happen between source and sink; confirm the exact context.
- **Remediation:** Apply context-appropriate validation/encoding at trusted boundaries and before dangerous sinks.

```text
SOURCE -> transform/store -> sink A
                    -> sink B
                    -> sink C
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
