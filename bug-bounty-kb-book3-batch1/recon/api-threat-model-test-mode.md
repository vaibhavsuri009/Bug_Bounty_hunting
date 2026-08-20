# API Threat-Model Test Mode

- What it is: Choose black-, gray-, or white-box testing based on the attacker knowledge you are modeling.
- Black box starts from minimal organizational information and emphasizes OSINT/recon.
- Gray box starts with approved targets, documentation, and usually a basic account.
- White box additionally uses source code, design details, SDKs, and internal implementation information.
- Build the attack-surface list appropriate to the chosen model before active testing.
- In black-box work, compile IPs, URLs, and API endpoints, then have the client confirm scope before attacking.
- False positive: discovering an asset does not mean it is authorized for active testing.
- Edge case: bug-bounty programs usually sit between black and gray box because scope and rules are provided.
- Remediation note: use the threat model to ensure security testing reflects realistic adversaries.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 0
