# Interactive Recon Loop

- What it is: Prompt for targets during execution and scan them until the operator exits.
- Where to look: Useful when manually triaging newly discovered domains one at a time.
- Read a domain from standard input:
```bash
echo "Please enter a domain!"
read INPUT
```
- Repeat until `quit`:
```bash
while [ "$INPUT" != "quit" ]; do
  read INPUT
  if [ "$INPUT" != "quit" ]; then
    scan_domain "$INPUT"
    report_domain "$INPUT"
  fi
done
```
- Combine with a `-i` flag parsed by `getopts` to enable interactive mode only when requested.
- False-positive/edge note: Validate input before passing it to shell commands; malformed values can break automation.
- Remediation: Not target-side; constrain interactive targets to authorized scope.

## Source: Bug Bounty Bootcamp, Ch. 5
