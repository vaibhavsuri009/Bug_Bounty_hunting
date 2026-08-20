# Clickjacking Frameability Test

- **What it is:** Checks whether a sensitive page can be embedded in a cross-origin iframe.
- **Where to look:** Pages containing state-changing buttons or controls that can be triggered by mouse clicks alone.
- First inspect response headers for `X-Frame-Options` and CSP `frame-ancestors`.
- Then confirm behavior with a local HTML test page.

```html
<html>
  <p>If the iframe renders, investigate further.</p>
  <iframe src="https://example.com/sensitive" width="500" height="500"></iframe>
</html>
```

- Use your own test account for any state-changing action.
- **False positives / edge cases:** A frameable read-only page without useful actions is usually not a meaningful clickjacking issue.
- **Remediation:** Set CSP `frame-ancestors` and/or `X-Frame-Options` appropriately on sensitive pages.

## Source: Bug Bounty Bootcamp, Ch. 8
