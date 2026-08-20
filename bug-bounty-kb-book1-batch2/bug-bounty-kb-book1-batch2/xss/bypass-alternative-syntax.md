# XSS Bypass: Alternative Syntax

- What it is: Bypass filters that block `<script>` by executing JavaScript through another HTML construct.
- Where to look: Inputs where the application removes or rejects script tags but still permits other markup/attributes.
- Example event-handler injection:
```html
<img src="123" onerror="alert('XSS')">
```
- Example executable link pattern:
```html
<a href="javascript:alert('XSS')">Click me!</a>
```
- Prefer payloads that fit the existing output context instead of forcing a new `<script>` element.
- Confirm that the event or navigation path is realistically triggerable by the affected user.
- False-positive/edge note: Filter bypass is meaningful only if JavaScript executes after all server/browser transformations.
- Remediation: Use contextual output encoding and structural allowlists rather than blocking only specific tags.

## Source: Bug Bounty Bootcamp, Ch. 6
