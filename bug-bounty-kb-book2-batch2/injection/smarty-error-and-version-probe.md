# Smarty SSTI Error + Version Probe

- What it is: A template error can reveal that user input is being parsed by Smarty even when a generic arithmetic payload fails.
- Submit a harmless template-style marker into a value reused by email/invite rendering.
- Inspect downstream errors/stack traces for `Smarty` parser or compiler references.
- The book then uses Smarty's reserved version variable:
```text
{$smarty.version}
```
- If the rendered output becomes a version number, Smarty evaluation is confirmed.
- Use this engine-specific probe before assuming a failed `{{7*7}}` means no SSTI.
- False positive: a stack trace mentioning Smarty may come from unrelated application code; confirm attacker-controlled evaluation.
- Edge case: syntax differs significantly between Smarty versions/configurations.
- Remediation: disable verbose template errors and never compile untrusted values as Smarty template source.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
