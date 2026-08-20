# CSRF + Self-XSS to Stored XSS

- **What it is:** Converts a self-only XSS into a remotely triggerable stored XSS by forging the vulnerable profile/update request.
- **Where to look:** User-editable fields that render unsafely but are normally writable only by the same user.
- Confirm the field has self-XSS using your test account.
- Check whether the update endpoint is vulnerable to CSRF.
- If yes, forge the update so the victim account stores the XSS payload automatically.

```text
CSRF -> write XSS payload into victim-owned field -> victim later views field -> XSS executes
```

- **False positives / edge cases:** If only the attacker ever views the field, impact remains self-XSS.
- **Remediation:** Fix output encoding/input handling and independently enforce CSRF protection on profile updates.

## Source: Bug Bounty Bootcamp, Ch. 9
