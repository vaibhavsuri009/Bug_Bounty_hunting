# PHP `call_user_func` Function Injection

- What it is: A user-controlled function name is passed to `call_user_func`, enabling unintended PHP functions.
- Look for parameters such as `action`, `function`, or handler names.
- Vulnerable pattern:
```php
$action = $_GET['action'];
$id = $_GET['id'];
call_user_func($action, $id);
```
- A read-only proof from the book uses `file_get_contents` with a test file.
- Confirm only the minimum function control needed to prove impact.
- False positive: an allowlist around `$action` can make dynamic dispatch safe.
- Edge case: PHP function availability and permissions vary.
- Remediation: map user actions to a fixed allowlist of application functions.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
