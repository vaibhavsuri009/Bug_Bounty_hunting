# Hidden ID Parameter Injection

- **What it is:** An endpoint that normally identifies the user from a session cookie may still accept undocumented object-ID parameters.
- **Where to look:** API endpoints that contain no visible ID but return user-specific resources.
- Start with the normal request.

```http
GET /api_v1/messages
```

- Add likely object-reference parameters manually: `id`, `user_id`, `message_id`, `account_id`, or similar.

```http
GET /api_v1/messages?user_id=ANOTHER_TEST_USER_ID
```

- Compare the returned data with the victim test account.
- Try query parameters and request-body parameters if the endpoint accepts both.
- **False positives / edge cases:** Ignore parameters that are accepted syntactically but do not alter authorization or returned objects.
- **Remediation:** Reject unauthorized object references and remove undocumented compatibility/test access paths.

## Source: Bug Bounty Bootcamp, Ch. 10
