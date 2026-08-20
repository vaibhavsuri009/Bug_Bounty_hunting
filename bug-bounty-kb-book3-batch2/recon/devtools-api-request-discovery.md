# DevTools API Request Discovery

- What it is: Browser DevTools exposes the background requests a web application makes to APIs.
- Open DevTools with `F12` or `Ctrl+Shift+I`, then refresh the target page.
- Start in the Network panel and filter for XHR/fetch/API-looking traffic.
- Click an interesting request and inspect its method, URL, headers, parameters, and response body.
- Correlate requests with actions you take in the UI to learn endpoint purpose.
- Use the Performance panel when you need to identify exactly when an API call fires.
- False positive: analytics/CDN requests may look API-like but be unrelated to the target’s business API.
- Edge case: lazy-loaded routes only appear after the related feature is used.
- Remediation note: backend authorization must not depend on endpoints being hidden from the UI.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
