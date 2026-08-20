# IDOR File Extension Bypass

- **What it is:** Authorization logic may differ depending on how a resource is referenced or which file representation is requested.
- **Where to look:** Endpoints that return JSON, files, exports, alternate formats, or REST-style representations.
- Start with an object request that is correctly blocked.

```http
GET /get_receipt?receipt_id=2983
```

- Add a file extension or alternate representation.

```http
GET /get_receipt?receipt_id=2983.json
```

- Compare authorization behavior between both requests.
- Test only alternate representations the application appears to support.
- **False positives / edge cases:** A different status code alone is insufficient; confirm that unauthorized victim data becomes accessible.
- **Remediation:** Apply identical authorization checks regardless of filename, extension, route alias, or representation.

## Source: Bug Bounty Bootcamp, Ch. 10
