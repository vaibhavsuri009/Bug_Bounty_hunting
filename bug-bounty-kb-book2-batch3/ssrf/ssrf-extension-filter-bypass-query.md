# SSRF Extension Filter Bypass with Query Delimiter

- What it is: A URL validator checks for an image-looking suffix but the parser treats that suffix as query data.
- The book's ESEA flow changed a path suffix into a query.
```text
http://host.example/1.png
http://host.example?1.png
```
- The second URL still contains `1.png` but requests the site root with `1.png` as a query string.
- Use this when the application insists the supplied URL "looks like" an image.
- False positive: robust validators parse the URL and verify the fetched content type.
- Edge case: null-byte and repeated-slash tricks may fail while query-delimiter parsing succeeds.
- Remediation: parse URLs structurally and validate the fetched response, not string suffixes.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
