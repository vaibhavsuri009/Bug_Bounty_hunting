# Reusable Recon Function Library

- What it is: Put common scan functions in a library and source them from multiple recon scripts.
- Where to look: Useful once the same Nmap, Dirsearch, crt.sh, or DNS logic appears in several tools.
- Example library structure:
```bash
nmap_scan(){ nmap $DOMAIN > $DIRECTORY/nmap; }
dirsearch_scan(){ dirsearch.py -u $DOMAIN -e php --simple-report=$DIRECTORY/dirsearch; }
crt_scan(){ curl "https://crt.sh/?q=$DOMAIN&output=json" -o $DIRECTORY/crt; }
```
- Load the functions from another script:
```bash
source ./scan.lib
```
- Keep shared paths and configuration centralized so tool changes require fewer edits.
- False-positive/edge note: Shell variables are generally global, but `$1`, `$2`, etc. inside a function refer to that function's arguments.
- Remediation: Not target-side; restrict write access to shared libraries so scan behavior cannot be silently altered.

## Source: Bug Bounty Bootcamp, Ch. 5
