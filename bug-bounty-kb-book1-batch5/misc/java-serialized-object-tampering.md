# Java Serialized Object Tampering

- If a Java serialized object controls identity or program state, modifying fields may alter application logic.
- After identifying and decoding/serializing the object format, inspect fields for usernames, roles, paths, and control values.
- Change one field at a time, reserialize the object, and replay it to the application.
- Example test ideas from the chapter: alter username/role markers in authentication objects or manipulate file/control-flow values.
- Compare authorization and application behavior before and after the modified object.
- A successful logic change indicates the server trusted client-controlled serialized state.
- False-positive trap: serialized objects may be signed/encrypted or validated against server-side state.
- Tools: proxy interception/replay plus the relevant Java serialization tooling or custom test program.
- Java serialized objects may be binary/non-printable, so edits usually require deserializing and reserializing rather than direct text replacement.
- Preserve the expected class and object structure when changing field values.
- Re-test the same request with the original object to establish a baseline.
- Remediation: store authoritative identity/session state server-side and never trust deserialized client fields for authorization.
## Source: Bug Bounty Bootcamp, Ch. 14
