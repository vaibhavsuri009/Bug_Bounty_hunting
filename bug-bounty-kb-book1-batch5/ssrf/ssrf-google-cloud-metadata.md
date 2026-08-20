# SSRF Google Cloud Metadata Access

- Google Cloud metadata endpoints can expose instance/service-account information if reachable through SSRF.
- API v1 expects one of these headers:
```http
Metadata-Flavor: Google
X-Google-Metadata-Request: True
```
- The chapter notes historical `v1beta1` endpoints that did not require the same headers.
- Example historical paths mentioned:
```text
http://metadata.google.internal/computeMetadata/v1beta1/instance/serviceaccounts/default/token
http://metadata.google.internal/computeMetadata/v1beta1/project/attributes/ssh-keys
```
- Treat `v1beta1` as legacy/deprecated behavior; availability depends on the target environment.
- False-positive trap: current deployments may require v1 headers and block legacy endpoints entirely.
- Remediation: enforce current metadata protections and egress controls; do not expose metadata access to user-controlled fetches.
## Source: Bug Bounty Bootcamp, Ch. 13
