# XML-Like Input Discovery

- What it is: XXE exposure is not limited to `.xml`; SVG, XML-based office formats, XFDF/PDF forms, RTF-like parsers, and legacy integrations may invoke XML parsers.
- Where to look / how to identify it:
  - Map endpoints that upload or transform XML-like files or accept `application/xml`/SOAP-style payloads.
- Exploitation / test pattern:
  - Start with harmless parser-identification probes and observe whether XML structure is processed.
- Tools + exact CLI syntax (if mentioned):
  - DevTools/Proxy plus file-format inspection.
- Common false-positive / WAF / edge-case notes:
  - Accepting XML is not a vulnerability; external entity resolution must be enabled or otherwise unsafe.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Disable external entities/DTDs unless required and use hardened parsers.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 12
