# Save Burp Requests as Reproducible Artifacts

- What it is: Preserve captured HTTP requests so they can be replayed, documented, or attached to a PoC.
- In Burp, right-click the request of interest.
- **Copy URL** saves only the request URL.
- **Copy as curl command** captures method, URL, headers, and body as a replayable command.
- **Copy to file** saves the full request to disk.
- Store artifacts in a target-specific notes directory.
- Use saved requests to reproduce findings without manually rebuilding the request.
- Keep separate files for interesting endpoints, recon results, draft reports, and PoCs.
- Record suspicious behavior even if it is not immediately exploitable.
- Track which features/endpoints were already tested to avoid duplicate work.
- False-positive trap: saved session cookies/tokens may expire; refresh authentication before assuming a finding no longer reproduces.
- Remediation: N/A — evidence and workflow technique.

## Source: Bug Bounty Bootcamp, Ch. 4
