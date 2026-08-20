# Unix Command Filter Bypass

- **What it is:** Equivalent shell syntax is used to evade filters that block literal command strings.
- **Where to look:** Command-injection points where a WAF or input validator rejects obvious keywords or paths.
- **Test / exploitation:**
  - Start from a confirmed injection point.
  - Insert quotes inside blocked words/paths; shell parsing may reconstruct the same token.
  - Try wildcards where the target path has predictable characters.
  - Try empty command substitutions inside the blocked word.
  - Compare blocked versus accepted forms and confirm with a harmless command.
- **Tools / syntax:**
```text
cat "/e"tc'/passwd'
cat /etc/pass*d
cat /etc/pass``wd
cat /etc/pass$()wd
```
- **False positives / edge cases:**
  - Bypass syntax depends on the shell and execution context; acceptance alone is not proof of execution.
- **Remediation:** Avoid shell parsing entirely; use safe APIs and server-side allowlists.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
