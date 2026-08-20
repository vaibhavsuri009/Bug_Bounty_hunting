# JavaScript and Data-URL XSS

- What it is: Abuse executable URL schemes when an application places attacker-controlled URLs into clickable or renderable contexts.
- Where to look: Profile-image URLs, redirect/link fields, previews, iframe sources, or any feature accepting arbitrary URLs.
- JavaScript scheme test:
```text
javascript:alert('XSS')
```
- Data URL test:
```text
data:text/html,<script>alert('XSS')</script>
```
- Base64-encoded data URLs can change how filters see the payload.
- Confirm that the application renders or navigates to the supplied URL in a browser-executable context.
- Test multiple browsers because scheme handling can differ.
- False-positive/edge note: Modern browsers restrict some schemes in particular tags/contexts; actual execution is required.
- Remediation: Allowlist expected URL schemes and destinations; never trust arbitrary executable schemes.

## Source: Bug Bounty Bootcamp, Ch. 6
