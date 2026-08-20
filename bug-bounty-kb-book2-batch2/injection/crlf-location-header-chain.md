# CRLF `Location` Header Injection Chain

- What it is: A CRLF flaw may be useful even when only additional headers—not a full response—can be injected.
- Look for a reflected value placed in a response header.
- Confirm line-break injection, then test a harmless `Location` header to your controlled test URL.
```text
%0D%0ALocation:%20https://example.test/
```
- Observe whether the browser follows the injected destination under the actual response status.
- This can convert a header-injection bug into open-redirect impact.
- False positive: an injected `Location` header does nothing if the response status/client behavior ignores it.
- Edge case: duplicate `Location` headers can be resolved differently by clients and proxies.
- Keep proof-of-concept destinations under your control and non-deceptive.
- Remediation: eliminate raw CR/LF and use strict allowlists for redirect destinations.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 6
