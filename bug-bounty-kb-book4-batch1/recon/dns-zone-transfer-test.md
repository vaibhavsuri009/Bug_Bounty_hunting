# DNS Zone Transfer Misconfiguration Test

- What it is: An improperly configured authoritative DNS server may return a zone file to an unauthorized requester.
- Where to look / how to identify it:
  - Identify the target's authoritative name servers, then request an AXFR/zone transfer only when explicitly authorized.
- Exploitation / test pattern:
  - Successful output may disclose hostnames and IP addresses useful for expanding the mapped attack surface.
- Tools + exact CLI syntax (if mentioned):
  - `host -t ns target.tld` then `host -l target.tld ns1.example.net`
- Common false-positive / WAF / edge-case notes:
  - A failed transfer is the expected secure result; a response from a secondary server may differ.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Restrict zone transfers to authorized secondary name servers using ACLs and authenticated DNS mechanisms.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
