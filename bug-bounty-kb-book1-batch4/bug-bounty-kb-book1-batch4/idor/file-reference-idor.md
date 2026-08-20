# File Reference IDOR

- **What it is:** Predictable filenames or paths expose files belonging to other users when file authorization is missing.
- **Where to look:** Download, upload, export, attachment, avatar, receipt, and document endpoints.
- Identify naming patterns such as `USER_ID-FILE_NUMBER.EXT`.
- Request a file owned by your attacker account.
- Change the filename or embedded user ID to one belonging to your victim account.

```http
GET /uploads?file=user1236-01.jpeg
```

- Check whether the server returns the victim-owned file without verifying ownership.
- Test only files belonging to your controlled accounts.
- **False positives / edge cases:** Public CDN-style files may be intentionally accessible without authorization.
- **Remediation:** Map file access to the authenticated user and enforce authorization before serving the file.

## Source: Bug Bounty Bootcamp, Ch. 10
