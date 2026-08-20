# XXE Local File Read

- What it is: An XML parser resolves an external entity pointing to a local file and inserts its contents.
- Look for XML bodies/uploads and XML-based formats processed server-side.
- Minimal pattern from the book:
```xml
<!DOCTYPE foo [
  <!ELEMENT foo ANY>
  <!ENTITY xxe SYSTEM "file:///etc/passwd">
]>
<foo>&xxe;</foo>
```
- Use a non-sensitive test file where the program provides one.
- False positive: seeing the entity text literally means external entities were not expanded.
- Edge case: parser configuration and file permissions determine read access.
- Remediation: disable external entity resolution/DTDs for untrusted XML.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 11
