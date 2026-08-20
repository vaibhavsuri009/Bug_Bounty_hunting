# PHP Magic-Method Deserialization RCE

- PHP `unserialize()` can automatically trigger magic methods such as `__wakeup()` and `__destruct()`.
- RCE becomes possible when attacker-controlled object properties flow into dangerous operations inside those methods.
- Vulnerable pattern shown in the chapter:
```php
function __wakeup(){
  if (isset($this->hook)) eval($this->hook);
}
$user_data = unserialize($_COOKIE['data']);
```
- Craft an object of the expected class and set the controlled property to a harmless proof-of-concept expression.
```php
private $hook = "phpinfo();";
```
- URL-encode the serialized object when inserting it into a cookie if required.
- Other useful magic methods mentioned: `__toString()` and `__call()`.
- Remediation: do not deserialize untrusted objects; remove dangerous sinks from magic methods and restrict allowed classes.
## Source: Bug Bounty Bootcamp, Ch. 14
