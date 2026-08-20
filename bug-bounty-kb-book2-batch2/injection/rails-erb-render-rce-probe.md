# Rails ERB Dynamic Render Code Execution Probe

- What it is: Historical dynamic render behavior could interpret attacker-controlled ERB as executable template source.
- Prerequisite: identify user input reaching Rails `render`, especially inline rendering.
- The book gives this encoded ERB example:
```text
<%25%3d`ls`%25>
```
- Decoded, it becomes an ERB expression that executes a shell command.
- For authorized testing, substitute a harmless non-destructive command/canary when possible.
- Modern Rails fixes CVE-2016-0752, so version and code path matter.
- False positive: seeing the payload reflected does not prove ERB evaluation.
- Edge case: `render inline:` remains dangerous when untrusted input is supplied as template text.
- Remediation: patch Rails and never pass untrusted strings into dynamic/inline template rendering.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
