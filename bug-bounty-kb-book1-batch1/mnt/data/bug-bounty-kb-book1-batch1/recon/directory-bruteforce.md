# Directory and File Brute-Forcing

- What it is: Request wordlist-derived paths to find hidden directories and files.
- Dirsearch example from the chapter:
```bash
./dirsearch.py -u target.example.com -e php
```
- Gobuster directory mode:
```bash
gobuster dir -u target_url -w wordlist
```
- Interpret common responses: `2xx` usually exists; `404` usually absent; `403` often exists but is access-controlled.
- Investigate `403` paths for legitimate authorization-bypass possibilities rather than discarding them.
- Look for admin panels, config files, backups, database copies, source files, old functionality, and directory listings.
- Path names can fingerprint technology, e.g. `phpmyadmin` suggests PHP tooling.
- Use screenshot tools such as EyeWitness or Snapper to triage many discovered pages quickly.
- Scope warning: directory brute-forcing is intrusive and can produce high request volume.
- False-positive trap: custom 404 pages may return `200`; compare body/length, not status alone.
- Remediation: remove sensitive files, disable directory exposure, and enforce authorization on hidden/admin content.

## Source: Bug Bounty Bootcamp, Ch. 5
