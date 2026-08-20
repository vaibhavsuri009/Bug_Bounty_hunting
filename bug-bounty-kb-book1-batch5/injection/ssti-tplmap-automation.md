# SSTI Automation with Tplmap

- Tplmap is mentioned as a tool for automating template-injection discovery and exploitation.
- It can help scan for SSTI, identify the template engine, and construct known exploit payloads.
- Use it only after mapping candidate user-input locations and confirming that automated testing is allowed by the program.
- The chapter does **not** provide exact tplmap CLI syntax, so no command is reproduced here.
- Manual confirmation remains important: establish the injection point and template behavior before trusting tool output.
- Engine coverage is incomplete; an unsupported engine can produce a false negative.
- Use safe PoCs when validating any command-execution capability.
- False-positive trap: tool-generated errors or reflected payloads do not prove server-side evaluation.
- The book presents tplmap as a follow-on efficiency tool rather than a substitute for understanding template syntax.
- Record the engine and injection context that the tool believes it detected, then verify manually.
- If automation fails, continue with the engine-specific probes described in the chapter.
- Remediation: separate untrusted data from template source, patch engines, and configure hardened sandbox/attribute allowlists.
## Source: Bug Bounty Bootcamp, Ch. 16
