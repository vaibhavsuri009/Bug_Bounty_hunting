# HTTP Method Fuzzing with Wfuzz

- What it is: Fuzz the HTTP verb to identify undocumented methods.
- Where to look / how to identify it:
  - `wfuzz -z list,GET-HEAD-POST-PUT-PATCH-TRACE-OPTIONS-CONNECT -X FUZZ http://testsite.com/api/v2/account`; use common `405` responses as baseline and inspect anomalies.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Accepted methods may still be generic no-op handlers.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Allow only required methods and authorize each independently.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
