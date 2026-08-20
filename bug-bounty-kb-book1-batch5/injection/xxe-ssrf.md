# XXE-to-SSRF

- External XML entities can turn an XXE into SSRF by requesting internal HTTP resources.
- Replace the entity's file URL with an internal host/port.
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE example [
  <!ENTITY file SYSTEM "http://10.0.0.1:80">
]>
<example>&file;</example>
```
- Vary internal hosts/ports and compare responses to map reachable services.
- Cloud metadata can also be targeted; the chapter shows AWS metadata URLs as an example.
- Inspect raw responses/page source for returned internal data.
- False-positive trap: XML entity resolution may allow local files but block HTTP/network schemes.
- Remediation: disable external entity resolution and restrict network egress from XML-processing services.
## Source: Bug Bounty Bootcamp, Ch. 15
