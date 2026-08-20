# SVG and Blob Script Risk

- What it is: SVG and Blob APIs can carry executable content and therefore should be treated as code-capable sinks.
- Where to look / how to identify it:
  - Review user-uploaded/generated SVGs and blobs that are later attached as script/image/document resources.
- Exploitation / test pattern:
  - Use non-executable formats for user media and block script-capable SVG features where not required.
- Tools + exact CLI syntax (if mentioned):
  - Content-type validation, CSP, sanitizer, upload pipeline.
- Common false-positive / WAF / edge-case notes:
  - SVG viewed as an image can behave differently from SVG embedded as active DOM.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Restrict active SVG, validate MIME/content, and avoid creating script blobs from user data.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
