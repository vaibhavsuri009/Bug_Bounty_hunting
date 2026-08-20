# XInclude File Read

- XInclude can be useful when you control only a fragment inserted into server-generated XML and cannot edit the DTD.
- Inject an `xi:include` element that requests a local file.
```xml
<example xmlns:xi="http://www.w3.org/2001/XInclude">
  <xi:include parse="text" href="file:///etc/hostname"/>
</example>
```
- Submit it into a field suspected of being embedded into backend XML.
- Check the raw response/output for the included file contents.
- This technique depends on the XML processor supporting and enabling XInclude.
- False-positive trap: ordinary XML parsing without XInclude support will simply reject or ignore the element.
- Remediation: disable XInclude where unnecessary and sanitize data before inserting it into XML structures.
## Source: Bug Bounty Bootcamp, Ch. 15
