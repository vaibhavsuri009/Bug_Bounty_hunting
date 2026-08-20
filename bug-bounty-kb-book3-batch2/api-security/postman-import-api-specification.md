# Import API Specifications into Postman

- What it is: Importing OpenAPI/Swagger/RAML/GraphQL specs turns documentation into ready-to-send requests.
- In Postman, use Import and provide a file, link, raw text, folder, or supported specification.
- Supported formats in the book include OpenAPI 3, RAML, GraphQL, Swagger, cURL, WADL, and others.
- After import, inspect collection variables such as `{{baseUrl}}`.
- Populate missing base URLs, tokens, IDs, and other required values.
- Run individual requests and compare behavior with the documentation.
- False positive: imported collections may be stale or point to retired hosts.
- Edge case: missing authorization is a common reason imported requests fail.
- Remediation note: keep published specs synchronized with deployed API behavior.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
