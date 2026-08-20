# Cross-Service SSTI via Email Rendering

- What it is: Input is harmless on one service but evaluated by a different template engine in an email or downstream system.
- Map where profile names, organization names, comments, and other values are reused.
- Store a harmless template probe such as `{{1+1}}`.
- Trigger downstream workflows: password/profile notifications, invitations, receipts, exports, or emails.
- In the book's Uber case, the profile displayed text normally while a notification email evaluated it to `2`.
- Follow with a slightly more complex harmless template construct to confirm real evaluation.
- False positive: a downstream system may replace the marker through unrelated formatting logic.
- Edge case: multiple subdomains/services can use different frameworks and trust each other's data.
- Document both the input source and the vulnerable render destination.
- Remediation: keep untrusted values as data across service boundaries and never concatenate them into template source.
- Check asynchronous workers and notification systems because the vulnerable renderer may execute minutes after input is stored.
- Use unique arithmetic values to distinguish real template evaluation from ordinary string substitution.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
