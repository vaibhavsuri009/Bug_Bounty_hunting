# Open Redirect Through a Trusted Third-Party Chain

- What it is: A trusted redirect path can become unsafe when it forwards into a third-party service that permits another redirect.
- Where to look: SSO/support/helpdesk/hosted-service links that the main site exempts from interstitial warnings or validation.
- Map every redirect hop rather than testing only the first destination.
- Identify whether a trusted service lets users control a later redirect or hosted page.
- In the book example, a trusted support flow reached a user-controlled hosted account whose JavaScript redirected again.
- Generic redirect script pattern:
```html
<script>document.location.href="https://attacker.example/";</script>
```
- Confirm the user reaches the final untrusted destination without the protection expected at the first hop.
- Edge case: The weakness may exist only because two otherwise legitimate services are chained together.
- False-positive trap: A normal external-link warning that remains visible through all hops may substantially reduce exploitability.
- Remediation: Validate every redirect hop and treat third-party destinations as external unless explicitly trusted.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 2
