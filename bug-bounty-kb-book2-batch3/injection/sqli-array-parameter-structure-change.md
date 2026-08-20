# SQLi via Array Parameter Structure Change

- What it is: Changing a scalar parameter into an array can alter how a framework builds SQL placeholders.
- Look for endpoints/frameworks that accept repeated or bracketed parameter syntax.
- The Drupal example highlights changing a normal parameter into an array.
```text
name=value
name[]=value
```
- Observe errors or query behavior changes when structure—not just value—is modified.
- This technique targets framework query-building assumptions rather than quote escaping.
- False positive: the application may simply coerce arrays to strings or reject them.
- Edge case: framework/version-specific behavior is critical.
- Remediation: validate parameter types and use patched framework/database APIs.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
