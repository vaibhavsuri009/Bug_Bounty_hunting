# Drupal `IN` Placeholder SQLi Pattern

- What it is: Historical Drupal query expansion trusted associative-array keys while constructing prepared-statement placeholders.
- The vulnerable logic concatenated attacker-controlled array keys into placeholder names.
```text
test);-- 
```
- A crafted key could transform an `IN (...)` clause and comment out the rest.
- This demonstrates that prepared statements fail if attacker input changes the statement template itself.
- Look for legacy Drupal 7.32-or-earlier systems only where testing is authorized.
- False positive: patched Drupal versions are not affected by this historical core flaw.
- Edge case: exploitation depends on array-parameter handling and PDO behavior.
- Remediation: upgrade Drupal and never incorporate untrusted identifiers/keys into SQL syntax.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
