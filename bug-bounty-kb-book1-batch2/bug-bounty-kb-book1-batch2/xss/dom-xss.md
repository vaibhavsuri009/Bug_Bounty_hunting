# DOM-Based XSS

- What it is: Client-side JavaScript places attacker-controlled data into the DOM in an executable way without server-side reflection.
- Where to look: URL parameters, fragments (`#...`), pathnames, and client-side code that dynamically rewrites HTML.
- Insert a unique marker into client-controlled sources and inspect the live DOM, not only the HTTP response.
- Example source pattern:
```text
https://example.com?locale=north+america
```
- If client code writes `locale` into HTML unsafely, test an execution payload appropriate to that sink.
- Compare the original HTTP response with the browser DOM; DOM XSS may leave the server response unchanged.
- Use browser developer tools to trace source-to-sink behavior and JavaScript errors.
- False-positive/edge note: A value present only in the URL is not enough; it must reach a dangerous DOM sink and execute.
- Remediation: Avoid unsafe DOM-writing APIs and validate/encode data before inserting it into the DOM.

## Source: Bug Bounty Bootcamp, Ch. 6
