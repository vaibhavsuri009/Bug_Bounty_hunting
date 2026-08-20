# XSS Input-Point Discovery

- What it is: Systematically find request values that are rendered into pages and may become XSS sinks.
- Where to look: Forms, searches, usernames, comments, profiles, dropdown values, numeric fields, URL parameters, fragments, and paths.
- Insert a unique marker such as `XSS_TEST_7421` into each input opportunity.
- Search returned page source for the marker to identify reflection points.
- For UI-restricted fields, intercept the request and modify the raw parameter directly.
- Example numeric-field bypass through a proxy:
```text
POST /edit_user_age
age=<script>alert('XSS')</script>
```
- Record the exact output context: HTML body, attribute, script block, URL, or DOM sink.
- False-positive/edge note: Client-side validation is not a security boundary; server-side rejection must also be tested.
- Remediation: Validate on the server and contextually encode all rendered untrusted values.

## Source: Bug Bounty Bootcamp, Ch. 6
