# postMessage Wildcard Target-Origin Leak

- **What it is:** A sender uses * as the postMessage target origin, allowing data to be delivered to an unintended window origin.
- **Where to look:** Cross-window/iframe communication that sends sensitive data using postMessage.
- **Test / exploitation:**
  - Inspect JavaScript for postMessage calls.
  - Look for a wildcard target origin in the second argument.
  - Create a page that can obtain the relevant window relationship and listen for message events.
  - Trigger the victim page to send the message.
  - Confirm whether your test page receives sensitive data.
- **Tools / syntax:**
```text
RECIPIENT_WINDOW.postMessage(MESSAGE_TO_SEND, "*");
```
- **False positives / edge cases:**
  - A wildcard is not impactful when the message contains no sensitive data and triggers no privileged action.
- **Remediation:** Specify the exact expected target origin.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 19
