# OSS Integration Risk Mapping

- What it is: Open source dependencies extend the application attack surface and may receive less review than first-party code.
- Where to look / how to identify it:
  - Inventory OSS dependencies, versions, integration method, privilege level, and data exchanged with the main application.
- Exploitation / test pattern:
  - Prioritize dependencies with large privilege, stale versions, complex transitive dependencies, or weak maintenance.
- Tools + exact CLI syntax (if mentioned):
  - BuiltWith/package manifests/source review.
- Common false-positive / WAF / edge-case notes:
  - OSS use is not itself a vulnerability; version, integration, and exposure determine risk.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain an SBOM, patch regularly, pin versions, and review high-risk integrations.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 17
