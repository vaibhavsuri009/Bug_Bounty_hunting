# Burp Decoder for Encoded Application Data

- What it is: Decode, alter, and re-encode application data found in requests or responses.
- Highlight the encoded value in a request/response.
- Right-click → **Send to decoder**.
- Choose an encoding/decoding algorithm from the Decoder controls.
- If the encoding is unknown, try **Smart decode**.
- Inspect the plaintext or decoded representation.
- Modify the decoded data when relevant to the assessment.
- Re-encode it using the corresponding encoding.
- Place the transformed value back into the request and test it with Proxy or Repeater.
- Useful targets include opaque-looking parameters, cookies, tokens, and serialized-looking values.
- False-positive trap: decoding readable text does not imply the value is unsigned or safely modifiable; verify server acceptance.
- Remediation: N/A — testing technique; protect security-sensitive client-controlled data with server-side validation/integrity controls.

## Source: Bug Bounty Bootcamp, Ch. 4
