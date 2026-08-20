# AngularJS Sandbox Escape Testing

- What it is: Older AngularJS Sandbox restrictions could be bypassed with version-specific expressions.
- Prerequisite: first confirm CSTI with a harmless expression such as `{{7*7}}`.
- Identify the exact AngularJS version before selecting a historical Sandbox bypass.
- The book includes this example for versions 1.3.0–1.5.7:
```text
{{a=toString().constructor.prototype;a.charAt=a.trim;$eval('a,alert(1),a')}}
```
- Use only a benign alert/origin proof in an authorized target.
- False positive: a payload copied for the wrong Angular version may fail even when CSTI exists.
- Edge case: application-side character filtering, CSP, or custom Angular hardening can prevent JavaScript execution.
- The arithmetic probe and the JavaScript escape should be reported as separate validation steps.
- Remediation: upgrade away from vulnerable AngularJS versions and avoid compiling untrusted strings as templates.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
