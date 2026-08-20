# Unicode Encoding Filter-Bypass Signal

- What it is: Equivalent JavaScript characters can be represented with Unicode escapes, bypassing filters that match only literal Latin strings.
- Where to look / how to identify it:
  - Inspect custom filters/blocklists for exact string matching against script/function names.
- Exploitation / test pattern:
  - Use harmless encoded strings to verify whether decoding later changes the effective code.
- Tools + exact CLI syntax (if mentioned):
  - Browser Console can validate Unicode decoding behavior.
- Common false-positive / WAF / edge-case notes:
  - Encoding acceptance alone is not exploitable without a script-capable sink.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Canonicalize input before validation and rely on safe sinks rather than blocklists.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
