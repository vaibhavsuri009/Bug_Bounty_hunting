# SSTI Input-Point Discovery

- Server-side template injection occurs when user input becomes template source code instead of template data.
- Enumerate every user-controlled location: URL path/query, fragments, request headers/body, file uploads, and stored profile/content fields.
- Prioritize inputs later rendered into dynamic pages, emails, reports, or files.
- Candidate locations often overlap with XSS sinks because both involve user-controlled rendered content.
- Capture the request for each candidate input and record where/when the value appears in generated output.
- Stored/delayed rendering matters: the injected template may execute in a future page, email, or generated file.
- Tools: Burp Proxy/Repeater for modifying parameters and tracing reflections.
- False-positive trap: reflection alone is not SSTI; the value must be evaluated by the template engine.
- Template-backed features commonly include customized home pages, bulk emails, and per-user content.
- Test both immediate reflections and data that is stored for later rendering.
- Keep a unique marker per field so you can trace which sink evaluated which input.
- Remediation: pass user data to templates only as data variables and never concatenate it into template source.
## Source: Bug Bounty Bootcamp, Ch. 16
