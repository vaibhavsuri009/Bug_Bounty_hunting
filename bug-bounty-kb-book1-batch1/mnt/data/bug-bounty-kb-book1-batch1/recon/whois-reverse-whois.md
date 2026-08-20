# WHOIS and Reverse-WHOIS Scope Discovery

- What it is: Use registration metadata to find domains tied to the same organization or owner.
- Query a known domain:
```bash
whois example.com
```
- Review registrant/organization/contact fields for ownership clues.
- Feed organization names, emails, or phone numbers into a reverse-WHOIS service.
- Use reverse WHOIS to discover obscure domains registered by the same owner.
- Add newly found domains only after confirming they are in program scope.
- Public reverse-WHOIS example mentioned: ViewDNS.info.
- Edge case: domain privacy services can replace real registrant details with proxy information.
- Edge case: shared registrars/contact data can create ownership false positives; corroborate with scope and other evidence.
- Remediation: N/A — public-registration reconnaissance; organizations can use privacy controls where appropriate.

## Source: Bug Bounty Bootcamp, Ch. 5
