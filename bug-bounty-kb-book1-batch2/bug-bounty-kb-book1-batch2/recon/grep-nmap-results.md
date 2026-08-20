# Parsing Nmap Output with grep

- What it is: Reduce raw Nmap output to the service/port lines most useful during recon triage.
- Where to look: Use after saving Nmap output to a file.
- Quick check for a specific port:
```bash
grep 80 TARGET_DIRECTORY/nmap
```
- Extract three-column service lines with extended regex:
```bash
grep -E '^\s*\S+\s+\S+\s+\S+\s*$' DIRECTORY/nmap > DIRECTORY/nmap_cleaned
```
- `-E` enables extended regular expressions.
- `\S+` matches non-whitespace fields; `\s+` matches separators.
- Use the cleaned file as input to a consolidated recon report.
- False-positive/edge note: Formatting changes or unusual Nmap output can break regex parsing; inspect raw output when results look incomplete.
- Remediation: Not target-side; this is analyst-side result processing.

## Source: Bug Bounty Bootcamp, Ch. 5
