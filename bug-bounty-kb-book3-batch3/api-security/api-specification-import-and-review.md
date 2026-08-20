# Import and Review API Specifications

- What it is: OpenAPI/Swagger/RAML/API Blueprint specs can reconstruct an API quickly.
- Where to look / how to identify it:
  - Find JSON/YAML/XML specs and markers like `"swagger":"2.0"`; Postman → Import → Link → spec URL; review routes/methods/headers/params and populate `baseUrl`/token variables.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Specs can omit live undocumented routes.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Synchronize deployed routes and published specs.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
