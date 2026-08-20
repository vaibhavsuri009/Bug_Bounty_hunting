# Client-Side HPP with Encoded Ampersand

- What it is: An encoded `&` can survive initial parsing and later become a new parameter in a generated URL.
- Where to look: User input that is embedded into links, share URLs, redirects, or other client-visible URLs.
- Submit a value containing `%26` followed by another parameter assignment.
- Example pattern:
```text
?par=123%26action=edit
```
- Inspect the generated HTML/link after the server processes the input.
- Determine whether `%26` becomes an effective `&` in the later URL and creates `action=edit` or another injected parameter.
- Test parameters that control actions, destinations, or object identifiers.
- False-positive trap: Seeing `&amp;` in HTML is not enough; verify the browser/server later treats it as a separate parameter.
- Remediation: Encode values for the final URL context and construct query strings with safe URL-building APIs.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 3
