# Netcat Callback Listener for RCE Proof

- What it is: Netcat can listen for HTTP callbacks carrying harmless command output from an authorized proof.
- The book's exact command is:
```bash
nc -l -n -vv -p 8080
```
- `-l`: listen mode.
- `-n`: disable DNS lookups.
- `-vv`: verbose output.
- `-p 8080`: listen on port 8080.
- Use a unique callback path/token when possible.
- False positive: unsolicited internet traffic can hit exposed listeners; correlate timing and content.
- Edge case: local firewall/NAT must allow the inbound connection.
- Remediation note: this is a testing utility, not a target-side fix.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
