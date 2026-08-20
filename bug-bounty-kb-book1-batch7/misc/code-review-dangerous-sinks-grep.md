# Code Review: Grep for Dangerous Sinks

- **What it is:** Fast white-box triage for functions that become dangerous when fed user-controlled data.
- **Where to look:** PHP `eval/assert/system/exec/shell_exec/passthru/popen/include/require/unserialize`; Python `eval/exec/os.system/pickle.loads/yaml.load`; Ruby command/deserialization functions.
- **Method:** Grep for sink names first, then trace each argument backward to request parameters, headers, cookies, files, or database data.
- **JavaScript sinks:** Review `document.write()` / `document.writeln()` for XSS and location-changing code for open redirects.
- **Exploit pattern:** User-controlled source → missing validation/encoding → dangerous sink.
- **False positives:** A dangerous function alone is not a vulnerability; confirm attacker control and reachable execution.
- **Remediation:** Remove dangerous sinks where possible; otherwise validate data and use safe APIs/allowlists.

```bash
grep -RniE 'eval\(|assert\(|system\(|exec\(|shell_exec\(|unserialize\(|pickle\.loads|yaml\.load|document\.write' .
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
