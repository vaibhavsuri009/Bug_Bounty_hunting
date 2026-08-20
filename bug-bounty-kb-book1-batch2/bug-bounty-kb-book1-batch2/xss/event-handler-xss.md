# Event-Handler XSS

- What it is: Execute JavaScript through HTML event attributes instead of a `<script>` element.
- Where to look: User input inserted inside existing HTML tags or attributes.
- Common event-handler pattern:
```html
<img src=x onerror=alert(1)>
```
- Other useful event attributes include `onload`, `onclick`, and `onmouseover` when their trigger condition is reachable.
- If input lands inside an existing tag, try adding a new event attribute rather than creating a new `<script>` block.
- Confirm the event actually fires in the victim-relevant interaction flow.
- This technique is especially useful when filters block the literal word `script`.
- False-positive/edge note: An event handler that requires unrealistic interaction may reduce severity.
- Remediation: Contextually encode attributes and prohibit attacker-controlled event-handler attributes.

## Source: Bug Bounty Bootcamp, Ch. 6
