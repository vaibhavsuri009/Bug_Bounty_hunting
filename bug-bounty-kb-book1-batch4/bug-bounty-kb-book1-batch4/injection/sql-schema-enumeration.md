# SQL Schema Enumeration

- **What it is:** After confirming SQL injection, metadata tables can reveal table and column names needed for targeted data access.
- **Where to look:** Confirmed injection points with enough output or a reliable blind oracle.
- For MySQL, enumerate user-defined table names from `information_schema.tables`.

```sql
UNION SELECT 1, table_name FROM information_schema.tables
```

- Then enumerate columns for a selected table.

```sql
UNION SELECT 1, column_name FROM information_schema.columns
WHERE table_name='Users'
```

- Adapt the metadata query to the identified database engine.
- **False positives / edge cases:** UNION column count/type mismatches can break otherwise valid payloads.
- **Remediation:** Prevent injection and restrict the application's database account to only required schemas/tables.

## Source: Bug Bounty Bootcamp, Ch. 11
