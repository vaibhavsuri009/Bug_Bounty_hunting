# Classic XXE File Read

- Classic XXE returns parser-resolved external entity data directly in the application response.
- First confirm entity processing, then try a local file via `SYSTEM`.
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE example [
  <!ENTITY test SYSTEM "file:///etc/hostname">
]>
<example>&test;</example>
```
- If `SYSTEM` fails, the chapter suggests trying `PUBLIC` with a dummy identifier.
- Common PoC targets mentioned: `/etc/hostname`, `/etc/passwd`, `~/.bash_history`.
- Inspect raw HTTP/page source because rendered HTML may hide or misrender the returned content.
- False-positive trap: file read depends on parser configuration and the web process's filesystem permissions.
- Remediation: disable DTD/external-entity resolution and use hardened XML parser settings.
## Source: Bug Bounty Bootcamp, Ch. 15
