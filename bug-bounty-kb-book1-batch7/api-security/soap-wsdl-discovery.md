# SOAP: WSDL Endpoint Discovery

- **What it is:** Use Web Services Description Language (WSDL) to enumerate SOAP operations and parameters.
- **Where to look:** SOAP services and older/IoT APIs that exchange XML.
- **Discovery patterns:** Append `.wsdl` or `?wsdl` to an API endpoint, or search URLs containing `wsdl`.
- **Method:** Retrieve the WSDL, enumerate operations/endpoints, then test each with the same authorization/input-validation methodology as other APIs.
- **False positives:** A published WSDL is not itself a vulnerability.
- **Edge case:** Internal/test WSDL documentation may expose endpoints absent from public docs.
- **Remediation:** Restrict sensitive service documentation and secure every documented operation server-side.

```text
https://target/service?wsdl
https://target/service.wsdl
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
