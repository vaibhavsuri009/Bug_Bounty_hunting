# Technology Stack Fingerprinting

- What it is: Identify server/framework/software brands and versions so testing can be targeted to relevant weaknesses.
- Run Nmap version detection:
```bash
nmap target.example.com -sV
```
- Review banners/service versions for exposed software and OS clues.
- Inspect HTTP response headers in Burp.
- Useful headers include `Server`, `X-Powered-By`, framework-specific headers, and technology-specific cookies.
- Example clues from the chapter: `PHPSESSID`, Drupal headers, Apache version strings.
- View page source and search for phrases such as `powered by`, `built with`, and `running`.
- Check framework-specific filenames/directories, e.g. `phpmyadmin` or template paths.
- Automation sources mentioned: Wappalyzer, BuiltWith, StackShare.
- Use confirmed versions to research relevant CVEs/misconfigurations before testing.
- False-positive trap: banners can be hidden, spoofed, stale, or fronted by reverse proxies; corroborate with multiple indicators.
- Remediation: reduce unnecessary version disclosure and keep exposed components/dependencies patched.

## Source: Bug Bounty Bootcamp, Ch. 5
