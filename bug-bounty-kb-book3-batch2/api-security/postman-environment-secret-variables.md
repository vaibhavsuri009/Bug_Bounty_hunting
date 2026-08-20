# Postman Environment Variables for API Testing

- What it is: Environment variables let multiple requests reuse URLs, IDs, and credentials safely.
- Create variables for base URL, token, user ID, tenant ID, and other repeated values.
- Use current/local values for sensitive data that should not be shared.
- Reference variables inside requests using Postman variable syntax.
- Maintain separate environments for production/test versions to compare behavior.
- Swap environments instead of manually editing every request.
- False positive: a stale environment variable can make a valid endpoint appear broken.
- Edge case: production and test APIs may unexpectedly accept the same token or resource IDs.
- Remediation: isolate environments and credentials; do not reuse production secrets in lower environments.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
