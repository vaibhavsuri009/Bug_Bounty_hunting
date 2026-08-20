# XXE Entry-Point Discovery

- XXE requires attacker-controlled XML reaching a parser with unsafe DTD/entity behavior.
- Search intercepted traffic for XML structure or the signature `<?xml`.
- Decode suspicious blobs; base64-encoded XML often starts with `LD94bWw` (base64 for `<?xml`).
- Inspect file-upload features because XML appears inside formats such as SVG, DOCX, PPTX, XLSX, GPX, PDF, RSS and image metadata.
- SOAP services are XML based and are also candidates.
- Try content-type switching on endpoints that normally accept plaintext/JSON:
```http
Content-Type: text/xml
Content-Type: application/xml
```
- Then send a minimal XML body and observe whether it is parsed.
- Remediation: disable DTD/external-entity processing and reject XML where it is not required.
## Source: Bug Bounty Bootcamp, Ch. 15
