# IDOR in Hidden Iframe Requests

- What it is: A page loads a secondary origin/endpoint in an iframe whose authorization parameters are easy to miss.
- Proxy the page and inspect all iframe/subresource requests.
- Review `src` URLs and parameters not visible in the browser address bar.
- Test account A's object/account identifier while authenticated as account B.
- The Binary.com example found a numeric `pin` in a cashier iframe flow.
- Burp Proxy history is useful for catching the secondary request.
- False positive: the iframe may expose only information already accessible to B.
- Edge case: iframe authentication can involve separate cookies/secrets.
- Remediation: authorize on the iframe backend endpoint, not only in the parent UI.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 16
