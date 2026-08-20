# Wayback Endpoint Discovery

- What it is: Use historical web archives to find removed or forgotten URLs that may still exist on the live target.
- Search the target in the Wayback Machine.
- Review older snapshots for endpoints, directories, subdomains, URLs, and files.
- Prioritize endpoints that disappeared from current navigation but may still respond.
- Record legacy paths for later authorization, input-validation, and version testing.
- Tool mentioned: Waybackurls for automatic extraction of archived endpoints/URLs.
- Feed archived URLs into your normal deduplication and live-host validation workflow.
- Compare current vs historical paths to spot deprecated functionality.
- Old directory listings and forgotten subdomains are particularly useful recon leads.
- False-positive trap: archived URLs may no longer exist, may now redirect, or may have moved out of scope.
- Remediation: fully retire deprecated endpoints and remove abandoned DNS/routes rather than merely unlinking them.

## Source: Bug Bounty Bootcamp, Ch. 5
