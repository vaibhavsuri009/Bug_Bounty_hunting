# Damn Vulnerable GraphQL Lab Setup

- What it is: DVGA is a deliberately vulnerable GraphQL target with an exposed GraphQL interface.
- Pull and launch:
```bash
sudo docker pull dolevf/dvga
sudo docker run -t -p 5000:5000 -e WEB_HOST=0.0.0.0 dolevf/dvga
```
- Browse to `http://localhost:5000`.
- Use the exposed GraphQL/GraphiQL functionality to practice discovery and request crafting.
- Keep the service restricted to an isolated lab.
- False positive: the application is intentionally vulnerable by design.
- Edge case: port 5000 may conflict with another local service.
- Remediation note: do not expose lab GraphQL IDEs or vulnerable containers publicly.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 5
