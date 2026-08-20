# Hidden Endpoint Discovery in JavaScript

- What it is: Frontend bundles reveal API paths and features not currently exposed in the UI.
- Search JavaScript for HTTP methods and strings such as `POST`, `DELETE`, `url:`, `/api/`, or feature names.
- Browser DevTools or Burp can search downloaded bundles.
- The book's HackerOne example exposed `/votes` POST/DELETE logic before the voting UI was enabled.
- Replay discovered endpoints only with your own authorized objects.
- Tools: JSParser is mentioned for tracking JavaScript files over time.
- False positive: dead code or future feature flags may point to endpoints that are disabled server-side.
- Edge case: minification/webpack chunks can obscure routes.
- Remediation: enforce backend authorization regardless of whether UI elements are hidden.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
