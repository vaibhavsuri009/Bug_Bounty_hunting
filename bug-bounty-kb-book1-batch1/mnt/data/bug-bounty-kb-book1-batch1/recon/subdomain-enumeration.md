# Subdomain Enumeration

- What it is: Discover subdomains to expand the web attack surface.
- Combine passive and brute-force tools rather than relying on one source.
- Tools mentioned: Sublist3r, SubBrute, Amass, Gobuster, Altdns.
- Gobuster DNS mode:
```bash
gobuster dns -d target_domain -w wordlist
```
- Merge/deduplicate wordlists:
```bash
sort -u wordlist1.txt wordlist2.txt
```
- Look for naming patterns such as `1.example.com`, `2.example.com`, `3.example.com`.
- Use Altdns to generate permutations from known subdomain names.
- Guess technology-based names, e.g. `jenkins.example.com` when Jenkins is known to be used.
- Recurse: enumerate discovered subdomains again to find hosts like `1.dev.example.com`.
- Wordlist source mentioned: SecLists; Commonspeak2 can generate current wordlists.
- False-positive trap: wildcard DNS can make many nonexistent names appear valid; verify hosts before testing.
- Remediation: N/A — reconnaissance; remove abandoned/unnecessary public DNS records where possible.

## Source: Bug Bounty Bootcamp, Ch. 5
