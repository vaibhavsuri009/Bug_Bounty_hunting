# Cross-API Scripting (XAS)

- What it is: XAS occurs when one API ingests unsanitized content from another service and later renders it in a browser.
- Where to look / how to identify it:
  - Using controlled third-party content, inject a harmless script marker into data that the target imports; observe whether the target renders/executes it; also test target API update routes feeding the UI.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Both the source API and target renderer must align; third-party rate limits may constrain testing.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Sanitize/encode all ingested third-party data before rendering.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
