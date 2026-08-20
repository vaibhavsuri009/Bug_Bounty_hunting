# Diff-Based Attack-Surface Monitoring

- What it is: Compare recon snapshots to surface newly exposed assets or functionality.
- Where to look: Best for recurring scans of domains, endpoints, JavaScript files, and subdomains.
- Compare two scan files:
```bash
git diff SCAN_1 SCAN_2
```
- Example scheduled comparison:
```cron
30 21 * * * ./scan_diff.sh facebook.com
```
- A simple script can print only changes between prior and current scan output.
- New assets are high-value because they may have weaker controls or newly introduced bugs.
- Version-controlled scan directories can also provide notifications when files change.
- False-positive/edge note: CDN churn, dynamic content, and reordered output can generate noisy diffs; normalize data first.
- Remediation: Continuously monitor internet-facing assets and decommission unintended exposure quickly.

## Source: Bug Bounty Bootcamp, Ch. 5
