# Isolate a Vulnerable API Lab

- What it is: Deliberately vulnerable targets should be separated from trusted home/work networks.
- Place each vulnerable application on an isolated VM/container network where possible.
- Prefer separate hosts for applications that may conflict or affect one another.
- Do not expose intentionally vulnerable services directly to the public internet.
- Snapshot lab VMs before testing destructive techniques.
- Restrict inbound/outbound networking to only what the lab exercise requires.
- False positive trap: a lab compromise can look like target behavior when another lab service was actually attacked.
- Edge case: cloud-hosted labs need security groups/firewalls preventing public exposure.
- Remediation note: isolation is the primary defense for intentionally vulnerable systems.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 5
