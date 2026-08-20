# Blind IDOR

- **What it is:** Unauthorized object access may succeed even when the HTTP response does not directly reveal the affected data.
- **Where to look:** Email receipts, exports, scheduled reports, notifications, text alerts, background jobs, and file-generation endpoints.
- Identify a request that references one of your own objects.

```http
POST /get_receipt
receipt_id=3001
```

- Replace the object ID with one from the victim test account.
- Send the request from the attacker session.
- Check secondary delivery channels such as your email inbox, export queue, or generated reports.
- Allow for delayed processing where applicable.
- **False positives / edge cases:** Confirm the delivered artifact belongs to the victim test account, not cached attacker data.
- **Remediation:** Apply authorization before queuing or generating any object-derived output.

## Source: Bug Bounty Bootcamp, Ch. 10
