# Read-Out-of-Bounds Length Mismatch

- What it is: The application reads more bytes than the actual attacker-supplied object contains.
- Look for protocol fields where the client supplies both data and a claimed length.
- Compare the declared length against the real payload size.
- Heartbleed's core pattern was trusting the request's length field rather than the actual heartbeat message size.
```text
actual message: 100 bytes
declared length: 1000 bytes
```
- A vulnerable implementation may return adjacent process memory.
- False positive: extra zero padding or a fixed error response does not prove arbitrary memory disclosure.
- Edge case: leaked bytes vary with process state and memory layout.
- Remediation: validate declared lengths against the actual received buffer before reading.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 13
