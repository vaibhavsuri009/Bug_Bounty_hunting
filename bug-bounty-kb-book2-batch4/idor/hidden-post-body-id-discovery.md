# Hidden POST-Body IDOR Discovery

- What it is: The object identifier is buried in request data or named something non-obvious.
- Proxy normal workflows and inspect every request parameter.
- Candidate names include `ref`, `user`, `column`, `administration_id`, and other integer/string references.
- Modify one parameter at a time in Burp Repeater.
- Observe whether the server accesses a different object without rechecking authorization.
- Do not rely on parameter names alone; numeric/string behavior can reveal identifier semantics.
- False positive: IDs can be lookup filters for already-public data.
- Edge case: nested JSON and multipart bodies often hide identifiers from the visible UI.
- Remediation: server-side authorization must be independent of obscurity or parameter location.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 16
