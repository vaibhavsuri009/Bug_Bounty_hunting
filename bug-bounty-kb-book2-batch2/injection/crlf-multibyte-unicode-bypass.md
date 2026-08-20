# CRLF Multibyte Unicode Blacklist Bypass

- What it is: A blacklist can miss a multibyte character that later decodes/strips into CR or LF bytes.
- Use this only after direct `%0D`/`%0A` input is clearly filtered.
- The book describes Unicode characters whose decoded low bytes produced `0A` and `0D`.
```text
%E5%98%8A
%E5%98%8D
```
- Submit a harmless header marker after the encoded pair and inspect the raw response.
- The important condition is inconsistent decoding/character stripping between validation and output.
- False positive: the multibyte sequence may be preserved or rejected, producing no CR/LF boundary.
- Edge case: behavior is highly dependent on legacy encoding stacks and is not portable across targets.
- Also test double encoding when the application performs multiple decode passes.
- Remediation: normalize to one canonical character set before validation and reject control characters after decoding.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 6
