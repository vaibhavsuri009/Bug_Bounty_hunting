# Blind SQLi Python Automation Pattern

- What it is: A script automates position/character testing against a blind SQLi oracle.
- The book uses Python with `requests`, JSON, Base64, and URL quoting.
```python
for pos in range(1, 31):
    for ch in charset:
        payload["user_id"] = f"5755 and mid(user(),{pos},1)='{ch}'#"
        # JSON -> Base64 -> URL encode -> GET
```
- Define a small expected character set to reduce requests.
- Use a deterministic success condition such as response length/content.
- Add delay/rate controls so automation stays within scope.
- False positive: an unstable response predicate can recover incorrect characters.
- Edge case: encoding order must match the original application workflow.
- Remediation: parameterize the vulnerable query and rate-limit only as defense in depth.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
