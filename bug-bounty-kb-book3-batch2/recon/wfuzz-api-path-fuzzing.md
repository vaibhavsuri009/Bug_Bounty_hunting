# Wfuzz API Path Fuzzing

- What it is: Wfuzz replaces `FUZZ` placeholders with payloads from a wordlist, list, or range.
- Basic file payload:
```bash
wfuzz -z file,/usr/share/wordlists/list.txt http://targetname.com/FUZZ
```
- Specify a method with `-X`, for example `-X POST`.
- Use `-z list,...` for explicit strings and `-z range,500-1000` for numeric IDs.
- Multiple payload positions can use multiple `-z` options and numbered fuzz markers.
- Filter noisy output by status, lines, words, or characters.
- False positive: soft-404s and generic error bodies can look like hits.
- Remediation: validate routes/parameters and enforce authorization independent of path guessing.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
