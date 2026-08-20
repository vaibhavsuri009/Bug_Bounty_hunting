# Self-Hosted Installer Risk

- What it is: One-click OSS installers may run privileged setup scripts that write files, configure databases, and alter server state.
- Where to look / how to identify it:
  - Look for self-hosted CMS/tools installed through setup scripts or package installers.
- Exploitation / test pattern:
  - Review the installer source and the privileges it requires before deployment or testing.
- Tools + exact CLI syntax (if mentioned):
  - Source review of setup scripts; package/vendor documentation.
- Common false-positive / WAF / edge-case notes:
  - Convenient installers are not automatically insecure; risk rises with privileged execution and opaque behavior.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Run installers with least privilege, verify signatures, review scripts, and isolate installation steps.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 17
