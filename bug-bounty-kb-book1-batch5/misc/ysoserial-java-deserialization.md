# Ysoserial Java Deserialization Payloads

- Ysoserial generates serialized exploit objects using known Java gadget chains.
- Generic syntax given in the chapter:
```bash
java -jar ysoserial.jar gadget_chain command_to_execute
```
- Example from the chapter:
```bash
java -jar ysoserial.jar CommonsCollections1 calc.exe
```
- Select a chain that matches libraries actually present in the target environment.
- Send the generated serialized object only through a confirmed user-controlled deserialization entry point.
- Use a harmless, reversible command for a bug-bounty PoC rather than modifying data or persistence.
- False-positive trap: ysoserial payload generation does not prove exploitability; the target must deserialize the object and contain the needed gadget classes.
- Remediation: avoid native deserialization of untrusted input and maintain strict class allowlists/dependency patching.
## Source: Bug Bounty Bootcamp, Ch. 14
