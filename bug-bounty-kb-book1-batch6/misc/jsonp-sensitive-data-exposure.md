# JSONP Sensitive Data Exposure

- **What it is:** A JSONP endpoint returns authenticated sensitive data as executable JavaScript that can be included cross-origin.
- **Where to look:** Endpoints accepting callback/jsonp parameters and returning user-specific data.
- **Test / exploitation:**
  - Look for script URLs containing callback or jsonp.
  - Request the endpoint with your own callback name.
  - Embed that URL in a script tag on a test page.
  - While logged into your test account, verify whether the browser sends credentials and the callback receives private data.
  - Treat JSONP on public data as non-sensitive.
- **Tools / syntax:**
```text
<script src="https://TARGET_URL?callback=parseinfo"></script>
```
- **False positives / edge cases:**
  - JSONP serving only public data is not a confidentiality issue.
- **Remediation:** Do not expose sensitive authenticated data through JSONP; use properly configured CORS instead.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 19
