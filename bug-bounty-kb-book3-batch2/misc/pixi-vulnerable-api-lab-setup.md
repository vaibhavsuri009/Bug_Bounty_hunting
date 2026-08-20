# Pixi Vulnerable API Lab Setup

- What it is: OWASP DevSlop Pixi provides a deliberately vulnerable MEAN-stack API target.
- Clone and launch:
```bash
git clone https://github.com/DevSlop/Pixi.git
cd Pixi
sudo docker-compose up
```
- Browse to `http://localhost:8000`.
- Use the app for API discovery, authorization, payment-system, and user-data testing.
- Keep it inside an isolated lab network.
- False positive: version drift may change ports or setup steps from the book.
- Edge case: Docker Compose syntax can differ on newer Docker releases.
- Remediation note: never expose this deliberately vulnerable target publicly.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 5
