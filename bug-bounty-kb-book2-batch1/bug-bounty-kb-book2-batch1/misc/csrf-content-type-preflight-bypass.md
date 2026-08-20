# CSRF Content-Type / Preflight Bypass

- What it is: An endpoint designed for JSON may also accept a simple form content type that avoids browser CORS preflight.
- Where to look: State-changing endpoints normally called with `Content-Type: application/json`.
- Replay the request using browser-simple content types:
```text
application/x-www-form-urlencoded
multipart/form-data
text/plain
```
- Preserve equivalent parameters/body semantics and check whether the endpoint still performs the action.
- If accepted, build a cross-origin form PoC using the accepted content type.
- Also inspect `Access-Control-Allow-Origin` behavior for arbitrary origins when evaluating related CORS exposure.
- Edge case: Some endpoints parse only JSON and will safely reject alternate encodings.
- False-positive trap: Avoid claiming CSRF merely because preflight disappears; the unauthorized state change must succeed.
- Remediation: Enforce the expected content type and independent CSRF/origin validation on state-changing requests.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 4
