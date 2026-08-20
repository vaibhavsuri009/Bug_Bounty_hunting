# Command Flag Injection After Shell Escaping

- What it is: Shell metacharacters are escaped, but attacker input is still passed as command-line arguments/flags.
- Look for code that relies only on helpers such as `escapeshellcmd`.
- Determine whether user input can begin with `-` and alter the invoked tool's behavior.
- Focus on harmless flags first, such as version/help/output-format switches.
- The book notes that escaping shell separators does not inherently stop flag injection.
- False positive: many commands terminate option parsing with `--` or validate the argument type.
- Edge case: impact is command-specific; some flags can write files or load configs.
- Remediation: pass arguments via safe APIs, validate them against an allowlist, and use `--` where supported.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
