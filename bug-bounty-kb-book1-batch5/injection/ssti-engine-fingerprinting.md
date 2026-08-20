# SSTI Template-Engine Fingerprinting

- After confirming SSTI, identify the template engine before building an engine-specific exploit.
- Error messages may directly disclose the engine, e.g. Jinja2 `UndefinedError`.
- Differential probes from the chapter:
```text
<%= 7*7 %>   -> ERB candidate if 49
${7*7}       -> Java/PHP-family candidate depending on context
{{7*7}}      -> Jinja2/Twig candidate if 49
{{7*'7'}}    -> Jinja2: 7777777 ; Twig: 49
```
- Use more than one probe because different engines share delimiters.
- Confirm with behavior rather than relying only on technology fingerprinting.
- False-positive trap: custom filters or preprocessing can transform payloads and mimic another engine.
- Remediation: update template frameworks and prevent user-controlled template source entirely.
## Source: Bug Bounty Bootcamp, Ch. 16
