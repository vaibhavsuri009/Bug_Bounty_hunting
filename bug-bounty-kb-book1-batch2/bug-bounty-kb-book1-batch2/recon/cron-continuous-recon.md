# Scheduled Continuous Recon with cron

- What it is: Run recon automatically at fixed intervals to detect changes in a target's attack surface.
- Where to look: Useful for long-running bug bounty programs where endpoints and subdomains change frequently.
- Edit the current user's crontab:
```bash
crontab -e
```
- Run a scan every day at 21:30:
```cron
30 21 * * * ./scan.sh
```
- Run every script in a recon directory:
```cron
30 21 * * * run-parts /Users/vickie/scripts/security
```
- Track new endpoints, JavaScript files, subdomains, and other assets between runs.
- False-positive/edge note: Scheduled active scans may violate program rate or automation rules; verify authorization first.
- Remediation: Not target-side; defenders should inventory exposed assets continuously and remove forgotten services.

## Source: Bug Bounty Bootcamp, Ch. 5
