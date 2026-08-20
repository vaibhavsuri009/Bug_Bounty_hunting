# SSTI Error-Probe Detection

- Inject syntax used by multiple template engines and look for template-specific evaluation errors.
- Test string recommended in the chapter:
```text
{{1+abcxx}}${1+abcxx}<%1+abcxx%>[abcxx]
```
- The deliberately undefined `abcxx` value is intended to trigger an engine error if the syntax is interpreted.
- A descriptive exception naming Jinja/Twig/FreeMarker/etc. strongly indicates template evaluation.
- If errors are suppressed, switch to arithmetic probes instead of concluding the endpoint is safe.
- Test stored/delayed outputs as well as the immediate HTTP response.
- Tools: Burp Repeater for repeatable single-parameter testing.
- Compare the same field with a plain marker first to establish normal behavior.
- Remediation: never build templates by concatenating user input; suppress detailed template-engine errors.
## Source: Bug Bounty Bootcamp, Ch. 16
