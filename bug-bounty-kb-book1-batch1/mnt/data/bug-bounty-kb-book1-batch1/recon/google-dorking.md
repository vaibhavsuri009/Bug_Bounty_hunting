# Google Dorking for Target Recon

- What it is: Use search-engine operators to find indexed assets, files, endpoints, and exposed information.
- Limit to target: `site:example.com`
- Find URL patterns: `inurl:"/course/jumpto.php" site:example.com`
- Find directory listings: `intitle:"index of" site:example.com`
- Find file types: `filetype:log site:example.com`
- Enumerate indexed subdomains: `site:*.example.com`
- Find Kibana-style paths: `site:example.com inurl:app/kibana`
- Find script/log files: `site:example.com ext:php` or `site:example.com ext:log`
- Combine terms: `site:example.com ext:txt password`
- Search third-party S3 presence: `site:s3.amazonaws.com COMPANY_NAME`
- Useful operators: `site`, `inurl`, `intitle`, `filetype`, quotes, `*`, `|`, and `-`.
- Edge case: heavy automated/manual dorking can trigger Google CAPTCHA, especially on shared networks.
- Remediation: remove sensitive indexed content and prevent secrets/logs/private directories from being publicly reachable.

## Source: Bug Bounty Bootcamp, Ch. 5
