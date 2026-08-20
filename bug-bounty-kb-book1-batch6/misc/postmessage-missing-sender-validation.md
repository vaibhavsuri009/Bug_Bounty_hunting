# postMessage Missing Sender-Origin Validation

- **What it is:** A message receiver processes arbitrary postMessage data without checking event.origin.
- **Where to look:** Pages with message event listeners that perform state changes or consume security-sensitive data.
- **Test / exploitation:**
  - Find message listeners in page source or browser developer tools.
  - Determine the message structure expected by the receiver.
  - Open or frame the target page to obtain its window reference.
  - Send a harmless test message from an untrusted origin.
  - Confirm whether the receiver performs the corresponding action.
- **Tools / syntax:**
```text
var recipient_window = window.open("https://TARGET_URL");
recipient_window.postMessage("RANDOM MESSAGE", "*");
```
- **False positives / edge cases:**
  - If the receiver validates event.origin before processing, the untrusted message should be ignored.
- **Remediation:** Validate event.origin against an exact trusted origin before acting on message data.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 19
