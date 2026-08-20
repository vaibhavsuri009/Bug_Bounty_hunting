# XML-to-Image Parser Chain

- What it is: Features that transform DOM/XML into images or documents can hide an XML parser behind an apparently unrelated utility endpoint.
- Where to look / how to identify it:
  - Look for screenshot, report, document conversion, SVG rendering, and XML-to-image workflows.
- Exploitation / test pattern:
  - Capture the conversion request and determine whether the server parses client-controlled XML.
- Tools + exact CLI syntax (if mentioned):
  - DevTools/Proxy request inspection.
- Common false-positive / WAF / edge-case notes:
  - The visible UI format may differ from the parser format used server-side.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Treat all conversion inputs as untrusted and harden the parser used by downstream libraries.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 12
