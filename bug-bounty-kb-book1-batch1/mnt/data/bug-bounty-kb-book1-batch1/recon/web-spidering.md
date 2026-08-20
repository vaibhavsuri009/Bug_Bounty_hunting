# Web Spidering / Crawling

- What it is: Recursively follow links to enumerate reachable pages, paths, and endpoints.
- Start from an in-scope URL.
- A spider extracts URLs from each page and recursively visits discovered links.
- OWASP ZAP includes a built-in spider.
- ZAP workflow: Tools → Spider → set starting URL → **Start Scan**.
- Review the discovered URLs in the results pane.
- Use the generated site tree to understand files/directories and application structure.
- Burp Suite provides a crawler as an alternative.
- Combine crawl output with proxy history and brute-force results to spot endpoints found by only one method.
- Scope warning: spidering actively generates requests and may be restricted by a bounty program.
- False-positive trap: crawlers can follow logout/destructive links or get trapped in infinite URL spaces; constrain scope carefully.
- Remediation: N/A — reconnaissance; sensitive functionality must rely on authentication/authorization, not obscurity.

## Source: Bug Bounty Bootcamp, Ch. 5
