# Wfuzz: IDOR/BOLA Enumeration

- **What it is:** Iterate candidate object IDs to identify unauthorized object access.
- **Where to look:** Numeric or enumerable `user_id`, `message_id`, document IDs, or resource paths.
- **Command pattern:** Put `FUZZ` where the identifier appears and use an ID wordlist.
- **Validation:** Compare status code/content length, then manually verify whether returned objects belong to other users.
- **False positives:** Valid public objects are not IDOR; verify ownership and authorization requirements.
- **Edge case:** Error pages may have similar lengths; compare semantic content as well.
- **Remediation:** Perform object-level authorization on every resource request.

```bash
wfuzz -w ids.txt http://example.com/view_inbox?user_id=FUZZ
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
