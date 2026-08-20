# Wfuzz Numeric-Range BOLA Probe

- What it is: Numeric fuzzing checks whether adjacent object IDs expose resources.
- Start with an endpoint containing an ID you own.
```bash
wfuzz -z range,500-1000 http://targetname.com/account?user_id=FUZZ
```
- Compare status, response size, and body content across IDs.
- Follow up interesting IDs manually using a second controlled account.
- Do not treat predictable IDs alone as BOLA.
- False positive: public objects can legitimately return across many IDs.
- Edge case: generic `200` responses may hide authorization errors in JSON.
- Remediation: enforce object-level authorization on each resource request.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
