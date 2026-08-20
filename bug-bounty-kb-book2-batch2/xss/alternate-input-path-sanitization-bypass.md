# XSS via Alternate Input Path

- What it is: One input channel sanitizes data, while another path stores the same field without equivalent validation.
- Map every way the application accepts a value: web form, JSON upload, API, import, mobile endpoint, etc.
- Submit the same benign XSS marker through each path.
```html
#"><img src=/ onerror=alert(document.domain)>
```
- The book's Google Tag Manager example was safe through a form but unsafe through JSON file upload.
- Focus on the final render sink, because output-time encoding would have protected every ingestion path.
- False positive: a payload that appears in stored JSON but is encoded at render time is not XSS.
- Edge case: validation can differ by API version, role, or content type.
- Tools: proxy plus file/API import features.
- Remediation: encode at output and centralize validation across all ingestion paths.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
