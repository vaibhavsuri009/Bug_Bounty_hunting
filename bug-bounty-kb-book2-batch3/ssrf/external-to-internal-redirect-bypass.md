# SSRF External-to-Internal Redirect Bypass

- What it is: A validator permits an external URL, but the server follows a redirect to an internal address.
- Prerequisite: the feature fetches your external server but blocks private IPs directly.
- Return a 30x response from your server pointing to an internal test address.
```http
HTTP/1.1 302 Found
Location: http://127.0.0.1/
```
- Test whether the target follows 301/302/303/307 redirects after validation.
- Confirm with harmless internal endpoints only.
- False positive: some clients expose the redirect but do not follow it.
- Edge case: validation may be repeated after redirects, which blocks the technique.
- Remediation: revalidate every redirect hop and block private/link-local destinations at the network layer.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
