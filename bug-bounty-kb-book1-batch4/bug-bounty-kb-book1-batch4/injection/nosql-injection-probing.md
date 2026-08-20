# NoSQL Injection Probing

- **What it is:** NoSQL query languages can interpret user-controlled operators or executable expressions when application input is not validated.
- **Where to look:** MongoDB, CouchDB, Cassandra, and other non-relational database-backed endpoints.
- Probe suspected inputs with syntax-significant characters.

```text
'  "  ;  \  ( )  [ ]  { }
```

- Compare errors and response behavior against a clean baseline.
- If MongoDB is identified, pay attention to operator injection such as `$ne` and server-side JavaScript features such as `$where`.
- **Tools:** The book mentions NoSQLMap for automating NoSQL injection testing.
- **False positives / edge cases:** Parser errors prove only that structured input reached a parser, not that arbitrary query logic is controllable.
- **Remediation:** Strictly validate types/structure and disable dangerous server-side scripting features when unnecessary.

## Source: Bug Bounty Bootcamp, Ch. 11
