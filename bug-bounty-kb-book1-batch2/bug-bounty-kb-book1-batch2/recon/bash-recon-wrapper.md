# Bash Recon Wrapper

- What it is: A shell wrapper that runs repeatable recon tools against a supplied target.
- Where to look: Use when the same Nmap/Dirsearch workflow must be repeated across targets.
- Pass the target as `$1` so the script is reusable instead of hard-coding a hostname.
- Minimal pattern:
```bash
#!/bin/bash
nmap $1
dirsearch.py -u $1 -e php
```
- Make the script executable before running it:
```bash
chmod +x recon.sh
./recon.sh scanme.nmap.org
```
- If a tool is outside `$PATH`, use its absolute path or export its directory into `$PATH`.
- False-positive/edge note: Tool output is only recon evidence; verify findings manually before treating them as vulnerabilities.
- Remediation: Not applicable to the target; keep automation scoped to authorized assets.

## Source: Bug Bounty Bootcamp, Ch. 5
