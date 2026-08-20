# Android: Frida Runtime Instrumentation

- **What it is:** Inject JavaScript into running app processes to observe or alter runtime behavior.
- **Use cases mentioned:** Inspect called functions, analyze network connections, and bypass certificate pinning.
- **Where it helps:** Dynamic validation after static code review identifies a suspicious function or security check.
- **Method:** Attach/instrument only a test instance, observe relevant calls, then validate whether controls can be bypassed.
- **Requirement:** Frida scripting uses JavaScript; prebuilt scripts can accelerate testing.
- **False positives:** Instrumentation can change app behavior; reproduce findings without unnecessary hooks where possible.
- **Remediation:** Keep sensitive authorization decisions server-side and harden client integrity checks.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
