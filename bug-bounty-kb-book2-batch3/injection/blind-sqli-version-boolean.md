# Blind SQLi Database-Version Boolean Test

- What it is: A Boolean expression tests one character of a DBMS-generated value.
- Prerequisite: a stable blind SQLi response oracle.
- The book uses MySQL `version()` and `mid()`:
```text
(2010)and(if(mid(version(),1,1))='5',true,false))--
```
- Compare the response with known-true and known-false controls.
- A matching response can reveal whether the tested character is correct.
- Repeat character-by-character only if deeper enumeration is in scope.
- False positive: syntax/function names vary between MySQL, PostgreSQL, MSSQL, etc.
- Edge case: application logic may normalize both true and false responses.
- Remediation: remove injection by parameterizing the underlying query.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
