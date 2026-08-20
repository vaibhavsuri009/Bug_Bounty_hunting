# PHP POP-Chain Deserialization

- Property-Oriented Programming (POP) chains reuse existing classes/methods as gadgets after unsafe deserialization.
- Start from an automatically invoked magic method such as `__wakeup()`.
- Trace attacker-controlled properties into another object/method, then toward a dangerous sink such as `eval()`.
- Chapter pattern:
```text
unserialize(user data)
 -> Example::__wakeup()
 -> $obj->evaluate()
 -> CodeSnippet::evaluate()
 -> eval($code)
```
- Build a serialized object graph using class/property names available in the target codebase.
- Set the final controlled property to a harmless PoC expression before serializing and URL-encoding it.
- False-positive trap: the required gadget classes must actually be loaded/available in the application environment.
- Remediation: eliminate untrusted deserialization and use strict class allowlists where deserialization is unavoidable.
## Source: Bug Bounty Bootcamp, Ch. 14
