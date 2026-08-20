# Burp HTTPS Interception

- What it is: Trust Burp as a local CA so the proxy can inspect HTTPS traffic.
- First route Firefox through `127.0.0.1:8080` while Burp is running.
- Browse to `http://burp/`.
- Click **CA Certificate** and save Burp's CA certificate.
- In Firefox: Preferences → Privacy & Security → Certificates → View Certificates → Authorities.
- Import the Burp CA certificate.
- Trust it to identify websites, then restart Firefox.
- In Burp Proxy, switch interception on.
- Browse to an HTTPS site and verify the request is captured.
- Troubleshooting: if HTTPS requests do not appear, reinstall the CA certificate and re-check proxy settings.
- Tools: Burp Suite + Firefox certificate store.
- Edge case: Burp's embedded browser is already configured for Burp traffic.
- Remediation: N/A — assessment environment setup.

## Source: Bug Bounty Bootcamp, Ch. 4
