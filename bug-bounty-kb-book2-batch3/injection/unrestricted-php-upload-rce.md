# Unrestricted PHP Upload to Code Execution

- What it is: A server stores attacker-uploaded PHP in a web-executable directory.
- Look for upload features that accept arbitrary extensions/content.
- The book's minimal shell pattern is:
```php
$cmd = $_GET['super_secret_web_param'];
system($cmd);
```
- In authorized testing, prefer a harmless static PHP proof instead of a reusable shell.
- Verify whether the uploaded file is interpreted as PHP when requested.
- False positive: upload success alone is not RCE if the file is served as inert text/download.
- Edge case: extension filtering may be bypassed or server execution disabled per directory.
- Remediation: store uploads outside web roots, randomize names, and never execute user-controlled files.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
