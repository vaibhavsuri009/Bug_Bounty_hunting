# Serializer Identification

- What it is: Serialization converts objects into transferable/storable formats such as JSON, XML, YAML, or encoded blobs.
- Where to look / how to identify it:
  - Identify endpoints and libraries that serialize/deserialze client-controlled objects.
- Exploitation / test pattern:
  - Compare normal input and serialized output using synthetic test objects.
- Tools + exact CLI syntax (if mentioned):
  - Source/dependency review and request inspection.
- Common false-positive / WAF / edge-case notes:
  - Serialization itself is normal; unsafe handling appears when crafted data changes code execution or object state.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use safe serializers, disable code-evaluating features, and validate schemas before deserialization.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 15
