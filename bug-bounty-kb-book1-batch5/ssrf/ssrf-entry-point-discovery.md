# SSRF Entry-Point Discovery

- SSRF occurs when user-controlled input makes the server fetch a URL or network resource.
- Look for features that retrieve external resources: webhooks, URL-based uploads, proxies, link previews, thumbnails, document/image processors.
- Also inspect hidden API endpoints accepting URLs and URLs embedded in XML/PDF or HTML-related input.
- Record every request where a parameter appears to contain an absolute/relative URL.
- Typical patterns:
```http
POST /webhook
url=https://attacker.example

POST /upload_profile_from_url
user_id=1234&url=https://attacker.example/profile.jpeg
```
- Tools: intercept requests with Burp Proxy/HTTP history.
- False-positive trap: server-side URL fetching alone is not enough; confirm access to unintended/internal resources or meaningful outbound behavior.
- Remediation: validate destination URLs and block access to local/private/internal resources; prefer strict allowlists where possible.
## Source: Bug Bounty Bootcamp, Ch. 13
