# Building a Master Recon Report

- What it is: Merge outputs from several recon tools into one timestamped report.
- Where to look: Useful after running Nmap, Dirsearch, and certificate-transparency enumeration.
- Create the report with a timestamp:
```bash
TODAY=$(date)
echo "This scan was created on $TODAY" > $DIRECTORY/report
```
- Append cleaned Nmap results:
```bash
grep -E '^\s*\S+\s+\S+\s+\S+\s*$' $DIRECTORY/nmap >> $DIRECTORY/report
```
- Append Dirsearch and crt.sh data:
```bash
cat $DIRECTORY/dirsearch >> $DIRECTORY/report
jq -r '.[] | .name_value' $DIRECTORY/crt >> $DIRECTORY/report
```
- False-positive/edge note: Only append outputs that exist; otherwise stale/missing modules can make a report misleading.
- Remediation: Not target-side; store reports securely because they map the target attack surface.

## Source: Bug Bounty Bootcamp, Ch. 5
