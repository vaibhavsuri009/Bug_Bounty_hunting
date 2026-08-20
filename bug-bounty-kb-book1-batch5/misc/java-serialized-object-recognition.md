# Java Serialized Object Recognition

- Java deserialization issues require finding user-controlled serialized objects reaching `ObjectInputStream.readObject()` or equivalent logic.
- Common Java serialization signatures from the chapter:
```text
AC ED 00 05   # hex prefix
rO0            # common base64 prefix
```
- Another indicator is:
```http
Content-Type: application/x-java-serialized-object
```
- Search cookies, HTTP parameters, headers, and request bodies; objects are often encoded before transmission.
- Source-code review: locate classes implementing `Serializable` and calls to `readObject()`.
- Local compilation commands shown:
```bash
javac SerializeTest.java
java SerializeTest
```
- Remediation: reject untrusted serialized objects and restrict deserialization to explicitly permitted classes/types.
## Source: Bug Bounty Bootcamp, Ch. 14
