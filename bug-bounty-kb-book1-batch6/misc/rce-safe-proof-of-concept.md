# Safe RCE Proof of Concept

- **What it is:** Minimal-impact commands demonstrate code execution without unnecessary access to sensitive data or destructive actions.
- **Where to look:** After RCE is confirmed on an authorized bug-bounty or assessment target.
- **Test / exploitation:**
  - Prefer whoami or ls for output-based RCE.
  - Prefer sleep 5 for blind RCE.
  - Optionally create a uniquely named empty file when allowed.
  - Document the exact request and result.
  - Do not escalate privileges or read sensitive customer data unless scope explicitly permits it.
- **Tools / syntax:**
```text
whoami
ls
sleep 5
touch rce_by_YOUR_NAME.txt
```
- **False positives / edge cases:**
  - Reverse shells and privilege escalation may violate program rules even when basic RCE testing is allowed.
- **Remediation:** Patch the root execution flaw and apply least privilege to limit impact.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
