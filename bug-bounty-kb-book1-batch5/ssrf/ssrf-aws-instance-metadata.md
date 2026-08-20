# SSRF AWS Instance Metadata Access

- On AWS EC2, SSRF may reach the link-local instance metadata service at `169.254.169.254`.
- Initial discovery endpoint from the chapter:
```text
http://169.254.169.254/latest/meta-data/
```
- Insert it into the vulnerable server-side fetch URL.
- High-value paths mentioned:
```text
/latest/meta-data/local-hostname/
/latest/meta-data/iam/security-credentials/ROLE_NAME
/latest/dynamic/instance-identity/document/
/latest/user-data/
```
- Metadata may expose internal host data or temporary cloud credentials depending on instance configuration.
- False-positive trap: modern metadata protections, network policy, or disabled metadata access can block these requests.
- Remediation: use hardened metadata-service settings and block unnecessary access to link-local metadata from application workloads.
## Source: Bug Bounty Bootcamp, Ch. 13
