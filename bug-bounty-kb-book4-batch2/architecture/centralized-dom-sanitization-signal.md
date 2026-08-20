# Centralized DOM Sanitization Signal

- What it is: A reusable safe DOM insertion helper is a strong architectural indicator that XSS defenses are centralized rather than reimplemented ad hoc.
- Where to look / how to identify it:
  - Look for helper methods that default to text insertion and explicitly mark raw HTML insertion as unsafe.
- Exploitation / test pattern:
  - Trace whether application components consistently use the centralized safe helper.
- Tools + exact CLI syntax (if mentioned):
  - Source review; book example uses `innerText` by default and DOMPurify for explicit HTML.
- Common false-positive / WAF / edge-case notes:
  - A helper only helps when it is actually used consistently.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Centralize safe DOM APIs, default to text, and require reviewed sanitization for HTML.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 7
