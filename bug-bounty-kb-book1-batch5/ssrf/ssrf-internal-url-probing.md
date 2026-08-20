# SSRF Internal URL Probing

- Test suspected server-side fetchers with internal/private destinations.
- Common initial targets mentioned in the chapter: `localhost`, `127.0.0.1`, `0.0.0.0`, `192.168.0.1`, `10.0.0.1`.
- Replace the normal external URL with an internal address and compare behavior.
```http
POST /webhook
url=https://192.168.0.1
```
```text
https://public.example.com/proxy?url=https://192.168.0.1
```
- Probe known service ports when permitted, e.g. `127.0.0.1:22`, and inspect returned banners/errors.
- A banner such as an SSH version is strong evidence the server connected internally.
- Tools: Burp Repeater for controlled request replay and response comparison.
- Edge case: several private ranges may need testing because the target network topology is unknown.
- Remediation: resolve destinations server-side and reject loopback, link-local, private, and other restricted ranges before connecting.
## Source: Bug Bounty Bootcamp, Ch. 13
