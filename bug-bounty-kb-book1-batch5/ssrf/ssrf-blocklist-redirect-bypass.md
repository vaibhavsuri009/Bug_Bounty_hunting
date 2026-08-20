# SSRF Blocklist Bypass via Redirect

- A blocklist that checks only the submitted URL can be bypassed if your external server redirects to a blocked internal address.
- First submit a URL you control:
```text
https://public.example.com/proxy?url=https://attacker.example/ssrf
```
- Host a redirect response on that path; the chapter uses PHP:
```php
<?php header("location: http://127.0.0.1"); ?>
```
- The submitted value contains no blocklisted internal address, but the HTTP client follows it after validation.
- Confirm whether redirects are followed and whether each hop is revalidated.
- False-positive trap: fetchers that disable redirects or validate every redirect destination are not vulnerable to this bypass.
- Remediation: canonicalize and validate every redirect hop before making the next request.
## Source: Bug Bounty Bootcamp, Ch. 13
