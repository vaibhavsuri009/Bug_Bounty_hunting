# SAST-Assisted Source Code Review

- **What it is:** Automate static analysis to surface suspicious data flows and dangerous functions for manual review.
- **Where it helps:** Large source trees where fully manual review is too slow.
- **Workflow:** Run a SAST tool, rank findings by attacker control + sink severity, then manually trace and validate.
- **Use with grep:** Fast keyword/sink searches can seed the deeper SAST review.
- **Strength:** Finds issues without executing the application.
- **False positives:** Static analysis frequently flags unreachable or already-sanitized paths; verify manually.
- **Remediation:** Fix confirmed root causes, then add rules/tests to prevent regression.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
