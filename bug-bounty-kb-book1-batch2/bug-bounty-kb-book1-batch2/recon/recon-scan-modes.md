# Selective Recon Scan Modes

- What it is: Use shell conditionals or `case` statements to run only the recon modules needed for a target.
- Where to look: Helpful when active scanning restrictions differ by scope or when a fast partial scan is needed.
- Example invocation patterns:
```bash
./recon.sh target.com nmap-only
./recon.sh target.com dirsearch-only
./recon.sh target.com crt-only
```
- Prefer a `case` statement when several modes exist:
```bash
case $2 in
  nmap-only) nmap_scan ;;
  dirsearch-only) dirsearch_scan ;;
  crt-only) crt_scan ;;
  *) nmap_scan; dirsearch_scan; crt_scan ;;
esac
```
- False-positive/edge note: A partial mode can miss assets; record which modules actually ran.
- Remediation: Not target-side; enforce scope controls in the automation before active scans execute.

## Source: Bug Bounty Bootcamp, Ch. 5
