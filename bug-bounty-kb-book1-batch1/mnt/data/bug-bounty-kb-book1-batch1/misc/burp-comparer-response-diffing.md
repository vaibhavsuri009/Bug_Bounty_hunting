# Burp Comparer Response Diffing

- What it is: Highlight byte/text differences between two requests or responses.
- Generate a baseline request/response.
- Generate a second result with one controlled input change.
- Highlight the relevant blocks.
- Right-click → **Send to comparer**.
- Compare the two blocks to identify exact differences.
- Use this to determine how a changed parameter affects the server response.
- Useful when responses are large and manual visual comparison is unreliable.
- Pair with Repeater for controlled A/B testing.
- Pair with Intruder to manually validate anomalous automated results.
- False-positive trap: timestamps, CSRF tokens, ads, request IDs, and other dynamic fields can create irrelevant diffs.
- Remediation: N/A — comparison/testing technique.

## Source: Bug Bounty Bootcamp, Ch. 4
