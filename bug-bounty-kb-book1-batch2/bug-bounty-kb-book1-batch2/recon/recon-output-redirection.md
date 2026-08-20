# Saving Recon Output with Redirection

- What it is: Redirect scanner output into per-target files so results can be parsed and compared later.
- Where to look: Useful when Nmap, Dirsearch, or other recon tools produce large terminal output.
- Core operators:
```bash
PROGRAM > file      # overwrite
PROGRAM >> file     # append
PROGRAM < file      # file as input
PROGRAM1 | PROGRAM2 # pipe output
```
- Example target directory and reports:
```bash
mkdir ${DOMAIN}_recon
nmap $DOMAIN > ${DOMAIN}_recon/nmap
dirsearch.py -u $DOMAIN -e php --simple-report=${DOMAIN}_recon/dirsearch
```
- Store paths and target names in variables to keep scripts maintainable.
- False-positive/edge note: `>` destroys prior file contents; use `>>` when historical data must be preserved.
- Remediation: Not target-side; protect stored recon data because it may contain sensitive asset information.

## Source: Bug Bounty Bootcamp, Ch. 5
