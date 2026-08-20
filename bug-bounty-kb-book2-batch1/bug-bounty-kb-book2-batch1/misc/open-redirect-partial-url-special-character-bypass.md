# Partial-URL Open Redirect Bypass

- What it is: Special URL characters can change how a hardcoded redirect prefix plus user input is interpreted.
- Where to look: Redirects where only a suffix/path/host fragment is controllable and the application prepends a trusted domain.
- First determine the final URL constructed by the application.
- Try characters that alter URL parsing, especially a period or `@`.
- Example pattern from a hardcoded host plus attacker suffix:
```text
http://mystore.myshopify.com + .attacker.com
=> http://mystore.myshopify.com.attacker.com/
```
- Verify the browser resolves the rightmost registrable domain to the attacker-controlled site.
- Try variations only where the target actually concatenates user input into the final destination.
- False-positive trap: A string containing the trusted domain is not necessarily hosted by the trusted domain.
- Remediation: Parse the final URL and compare its normalized host against an exact allowlist.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 2
