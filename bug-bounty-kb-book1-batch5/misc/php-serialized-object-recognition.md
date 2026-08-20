# PHP Serialized Object Recognition

- PHP object injection starts with identifying user-controlled data passed to `unserialize()`.
- PHP serialization commonly follows `type:data` formatting.
- Object example from the chapter:
```text
O:4:"User":2:{s:8:"username";s:6:"vickie";s:6:"status";s:9:"not admin";}
```
- Useful markers: `b` Boolean, `i` integer, `d` float, `s` string, `a` array, `O` object.
- Large opaque request values may be base64-encoded serialized data; decode suspicious blobs before analysis.
- Source-code hunting: search for `unserialize()` receiving user-controlled cookies, parameters, or database values.
- CLI shown in the chapter for local PHP testing:
```bash
php serialize_test.php
```
- Remediation: avoid deserializing untrusted objects; use safer primitive data formats and server-side session state.
## Source: Bug Bounty Bootcamp, Ch. 14
