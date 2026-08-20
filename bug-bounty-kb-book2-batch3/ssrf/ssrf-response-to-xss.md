# SSRF Response-to-XSS Chain

- What it is: A server fetches attacker-controlled content and later renders that content as HTML.
- Point the SSRF fetcher at your controlled response server.
- Return a harmless HTML/XSS marker.
```html
<img src=x onerror=alert(document.domain)>
```
- Determine whether the fetched response is stored, reflected, or treated as an image/file.
- Confirm execution occurs in the vulnerable application's origin.
- False positive: rendering the payload as text or in an isolated origin is not target XSS.
- Edge case: content-type sniffing and CSP can affect execution.
- Remediation: never directly render fetched remote content; validate media types and serve it from an isolated origin.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
