# Python eval() Code Injection

- **What it is:** Unsanitized user input is passed to Python eval(), allowing input to be interpreted as Python code.
- **Where to look:** Calculator/expression features, dynamic rules, filters, or code paths where supplied expressions are evaluated.
- **Test / exploitation:**
  - Start with a harmless arithmetic expression and observe whether the server evaluates it.
  - Try a benign Python expression that produces recognizable output.
  - If execution context allows imports, test a harmless OS command such as ls.
  - For blind behavior, use a short sleep and compare response time.
  - Use harmless proof only; do not modify target data.
- **Tools / syntax:**
```text
print("RCE test!")
__import__('os').system('ls')
__import__('os').system('sleep 10')
```
- **False positives / edge cases:**
  - A reflected payload is not code execution unless its evaluated result or side effect is observable.
- **Remediation:** Do not pass untrusted input to eval(); parse expected expressions with safe, constrained logic.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
