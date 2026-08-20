# Burp Proxy Request Tampering

- What it is: Intercept a live HTTP request, modify it before delivery, then observe server behavior.
- Turn **Intercept is on** in Burp Proxy.
- Trigger the target action in the browser.
- Inspect URL path, query parameters, headers, cookies, and body values.
- Modify one security-relevant value at a time.
- Click **Forward** to send the altered request.
- Compare the browser/server result with the original request.
- Example pattern from the chapter: alter a user identifier in both URL and cookie to test object access.
- Example header test: change `Accept-Language: en-US` to another value and observe response behavior.
- Right-click a request and send it to Repeater/Intruder for deeper testing.
- Use the Proxy search bar to locate strings in captured requests/responses.
- False-positive trap: change only the field under test where possible so unrelated differences do not confuse results.
- Remediation: validate authorization and security-sensitive request data server-side.

## Source: Bug Bounty Bootcamp, Ch. 4
