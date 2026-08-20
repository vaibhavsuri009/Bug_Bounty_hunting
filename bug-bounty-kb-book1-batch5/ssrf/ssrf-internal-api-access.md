# SSRF Internal API Access

- A confirmed SSRF can sometimes call internal APIs that trust requests from internal network addresses.
- First map reachable internal hosts/services and identify API paths from recon or information leaks.
- Then request the internal endpoint through the SSRF primitive.
```text
https://public.example.com/send_request?url=https://admin.example.com/delete_user?user=1
```
- The security issue is the ability to cross an internal trust boundary, not merely fetch an external URL.
- Prefer non-destructive test endpoints/operations when validating impact.
- Credentials exposed through metadata or outbound headers may further expand reachable internal resources.
- False-positive trap: internal endpoints may still enforce user authentication/authorization even when reached from a trusted host.
- Internal-only trust based on source IP is especially relevant to this chain.
- Remediation: require strong authentication/authorization for internal APIs and remove network location as the sole trust signal.
## Source: Bug Bounty Bootcamp, Ch. 13
