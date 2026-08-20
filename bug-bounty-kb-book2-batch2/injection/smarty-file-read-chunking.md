# Smarty/PHP File-Read Chunking

- What it is: Output-length limits can hide a successful server-side file read, so reading a small bounded slice proves capability.
- Prerequisite: authorized Smarty/PHP code execution must already be confirmed.
- The book first attempts a full read, then limits the read to 100 bytes.
```text
{php}$s=file_get_contents('/etc/passwd',NULL,NULL,0,100);var_dump($s);{/php}
```
- A bounded read is safer and easier to fit into constrained renderers such as invitation emails.
- Prefer a non-sensitive test file when the program provides one.
- False positive: blank output can be caused by rendering/length limits rather than failed execution.
- Edge case: file permissions, disabled PHP functions, and template restrictions may block reads.
- Stop after minimal impact proof unless the program explicitly authorizes deeper access.
- Remediation: remove template code execution, sandbox the renderer, and run it with least filesystem privilege.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
