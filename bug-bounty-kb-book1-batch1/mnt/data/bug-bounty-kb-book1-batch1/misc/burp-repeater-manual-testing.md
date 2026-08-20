# Burp Repeater Manual Request Testing

- What it is: Manually resend and modify one HTTP request to isolate application behavior.
- Capture an interesting request in Proxy.
- Right-click → **Send to repeater**.
- Change one parameter, header, cookie, path component, or body value.
- Click **Send**.
- Inspect the response on the right side.
- Repeat with small controlled mutations.
- Use it for manual exploitation, filter-bypass testing, and alternate attack variants on one endpoint.
- Keep promising requests in Repeater as bookmarks for later testing.
- Prefer Repeater when precision matters; use Intruder when you need many automated variants.
- False-positive trap: dynamic tokens or expired sessions can change responses independently of your mutation.
- Remediation: N/A — testing technique; remediate the specific server-side flaw confirmed.

## Source: Bug Bounty Bootcamp, Ch. 4
