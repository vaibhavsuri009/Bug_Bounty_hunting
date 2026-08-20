# DevTools Source Secret and Endpoint Search

- What it is: Frontend source files may reveal API endpoints, tokens, keys, and internal feature names.
- Open DevTools → Sources and inspect JavaScript bundles and configuration files.
- Search for terms such as `api`, `key`, `secret`, `token`, `auth`, and versioned paths.
- Cross-reference discovered strings with Network-panel traffic.
- Treat any hardcoded credential as a lead and validate it minimally within scope.
- Search minified bundles even if the endpoint is not linked in the visible UI.
- False positive: demo/example keys or dead endpoints can remain in old bundles.
- Edge case: source maps can expose more readable code and original filenames.
- Remediation: never ship secrets to client-side code; rotate any exposed credentials.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
