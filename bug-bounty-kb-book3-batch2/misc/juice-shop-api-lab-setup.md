# OWASP Juice Shop API Lab Setup

- What it is: Juice Shop is a deliberately vulnerable REST-powered web application.
- Pull and launch the container:
```bash
docker pull bkimminich/juice-shop
docker run --rm -p 80:3000 bkimminich/juice-shop
```
- Browse to `http://localhost`.
- The port mapping avoids conflict with other apps using container port 3000.
- Use Burp/DevTools to discover the REST requests behind the UI.
- False positive: challenge behavior is intentionally insecure and should not be generalized as a production finding.
- Edge case: use a different host port if port 80 is already occupied.
- Remediation note: keep the target isolated from untrusted networks.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 5
