# Wfuzz Deep JSON-Body Fuzzing

- What it is: Wfuzz can send a large wordlist through JSON body fields.
- Where to look / how to identify it:
  - Pattern: `wfuzz -z file,big-list-of-naughty-strings.txt -H "Content-Type: application/json" -H "x-access-token: TOKEN" --hc 400 -X PUT -d '{"name":"FUZZ"}' -u http://TARGET/api/user/edit_info`; add `-p 127.0.0.1:8080` to proxy via Burp.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Filtering 400s can hide useful validation errors.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Strict JSON schema/type/length validation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
