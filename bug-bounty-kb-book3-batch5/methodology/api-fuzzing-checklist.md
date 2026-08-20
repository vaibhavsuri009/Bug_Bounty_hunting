# API Fuzzing Checklist

- What it is: Fuzzing should cover all accepted input locations while comparing results against a known baseline.
- Where to look / how to identify it:
  - Start broad with generic payloads, then target the technologies indicated by errors and recon.
- Exploitation / test pattern:
  - Use wide fuzzing for collection-level issues and deep fuzzing for individual high-value requests.
- Tools + exact CLI syntax (if mentioned):
  - Book tools: Postman Collection Runner, Burp Intruder/Comparer, Wfuzz.
- Common false-positive / WAF / edge-case notes:
  - Large request counts can trigger bans or DoS; stay within explicit testing limits.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Validate input types and lengths, handle errors safely, and apply rate limits.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. A
