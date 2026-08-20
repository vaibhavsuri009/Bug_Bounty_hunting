# SSRF GET vs POST Capability Check

- What it is: SSRF impact depends partly on which HTTP method and body the attacker can control.
- After confirming a fetch, determine whether it is GET-only or supports POST.
- Inspect webhook/import configuration for custom body, headers, or method settings.
- GET SSRF commonly supports retrieval and internal reconnaissance.
- POST SSRF may reach state-changing internal APIs when body parameters are attacker controlled.
- Record the exact method, headers, body, and redirect behavior.
- False positive: a UI labeled "webhook" may still enforce a fixed safe request template.
- Edge case: method restrictions can vary by destination scheme or feature.
- Remediation: use fixed request templates and isolate fetcher services from sensitive internal networks.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
