# HTTP Parameter Pollution: Hidden Parameter Injection

- What it is: Supplying a parameter the visible request normally omits can interfere with backend defaults or positional processing.
- Where to look: Workflows where the server appears to derive an important value internally, such as the current account or user ID.
- Capture the normal request and infer which values the server may be adding behind the scenes.
- Add plausible hidden parameters manually, for example:
```text
?to=67890&amount=5000&from=ABCDEF
```
- Observe whether the added value changes the operation despite not being present in the normal request.
- Test parameter ordering because backend arrays or parsers may rely on positional values.
- Compare server behavior with and without the injected field.
- False-positive trap: An ignored extra field is normal; impact requires it to influence a protected action.
- Remediation: Build trusted server-side values independently from attacker-controlled parameter collections.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 3
