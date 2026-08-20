# Python Code-Execution Filter Bypass

- **What it is:** Python string concatenation or escapes reconstruct blocked module/function names after input filtering.
- **Where to look:** Confirmed Python code injection where filters block literal module names such as os.
- **Test / exploitation:**
  - Confirm Python expression execution.
  - Split blocked strings with concatenation.
  - Try hexadecimal escape sequences for blocked module names.
  - Keep the system command harmless.
  - Compare parser behavior before and after server-side decoding.
- **Tools / syntax:**
```text
__import__('os').system('ls')
__import__('o'+'s').system('ls')
__import__('\x6f\x73').system('ls')
```
- **False positives / edge cases:**
  - A WAF bypass without successful downstream evaluation is not RCE.
- **Remediation:** Remove dynamic evaluation of untrusted input; do not depend on keyword filters.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
