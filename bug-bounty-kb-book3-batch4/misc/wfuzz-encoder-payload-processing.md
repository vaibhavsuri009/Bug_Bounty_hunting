# Wfuzz Encoder Payload Processing

- What it is: Wfuzz can encode payloads automatically before sending them.
- Where to look / how to identify it:
  - List encoders with `wfuzz -e encoders`; encode a file payload using `wfuzz -z file,wordlist/api/common.txt,base64 http://hapihacker.com/FUZZ`; use `base64-md5-none` for separate variants or `base64@random_upper` for chained processing.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Encoded variants can change request count dramatically.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Normalize encoded input before validation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
