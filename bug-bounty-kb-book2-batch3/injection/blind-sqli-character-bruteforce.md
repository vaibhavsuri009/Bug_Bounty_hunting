# Blind SQLi Character-by-Character Extraction

- What it is: A Boolean oracle is used to derive a string one character at a time.
- First identify a harmless metadata target such as DB user/host or database name.
- The book uses `mid()` to test each position against a candidate character set.
```text
5755 and mid(user(),1,1)='a'#
```
- Iterate positions, then candidate characters until the positive response is observed.
- Automate only within the program's rate limits and data-access rules.
- Stop once enough metadata is recovered to prove impact.
- False positive: response-length differences may be unstable; use repeated controls.
- Edge case: `#` is MySQL-specific comment syntax and may need URL encoding.
- Remediation: parameterized queries remove the oracle entirely.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
