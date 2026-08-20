# Android: Bypass Certificate Pinning with Frida/Objection

- **What it is:** Disable app-level certificate pinning in an authorized test environment to inspect HTTPS traffic.
- **When to suspect it:** Browser/device proxying works but the target app’s HTTPS traffic is missing or fails.
- **Tools mentioned:** Frida + Universal Android SSL Pinning Bypass script, or Objection (built on Frida).
- **Exact Objection command from source:** `android sslpinning disable`.
- **Custom pinning:** Automated bypasses may fail; manual patching of packaged certificates or validation code may be required.
- **False positives:** Network/security configuration problems can resemble pinning failures.
- **Remediation:** Pinning is a defensive control; ensure legitimate apps implement validation correctly and resist tampering.

```text
android sslpinning disable
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
