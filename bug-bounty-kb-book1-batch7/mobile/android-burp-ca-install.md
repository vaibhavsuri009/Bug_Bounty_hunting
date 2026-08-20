# Android: Install Burp CA for HTTPS Interception

- **What it is:** Trust Burp’s CA certificate on the Android test device so HTTPS can be decrypted by the proxy.
- **Where to get it:** While using Burp as the proxy, visit `http://burp/cert` and save the certificate.
- **Install path:** The book describes Android Security settings → Install Certificates from Storage.
- **Certificate use:** Select the option applicable to VPN/apps when prompted.
- **Validation:** HTTPS requests from the device should become readable in Burp.
- **Edge case:** Apps using certificate pinning will still reject the proxy certificate.
- **Remediation:** This is a testing setup technique; production apps may intentionally pin certificates.

```text
Device -> Burp proxy -> HTTPS target
       trusts Burp CA
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
