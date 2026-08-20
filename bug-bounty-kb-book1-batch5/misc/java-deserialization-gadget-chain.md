# Java Deserialization Gadget Chains

- Java deserialization RCE often requires chaining methods from classes already loaded by the application.
- After confirming untrusted deserialization, identify available libraries and search them for known gadget chains.
- Common libraries named in the chapter include Commons-Collections, Spring Framework, Apache Groovy, and Commons FileUpload.
- The chain should start from deserialization-triggered behavior and end at a command/code-execution sink.
- Recon matters: an exploit chain works only if its required classes are present in the target classpath.
- Prefer a non-destructive command or other harmless proof of execution when validating in authorized scope.
- False-positive trap: a published chain for a library/version not present on the target will fail.
- Tools: ysoserial is specifically recommended for generating known gadget-chain payloads.
- First identify the serialization entry point and confirm that arbitrary compatible classes can be instantiated.
- Map the dependency/library versions exposed by the application before selecting a known chain.
- A gadget chain is a sequence of existing methods, not attacker-uploaded classes.
- Remediation: eliminate untrusted native deserialization, patch dependencies, and restrict deserializable classes.
## Source: Bug Bounty Bootcamp, Ch. 14
