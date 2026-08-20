# Netdiscover Local Lab Host Discovery

- What it is: Netdiscover uses ARP discovery to identify hosts on the local lab network.
- Run a baseline before powering on the target, then run it again after startup.
```bash
sudo netdiscover
```
- Compare host lists and identify the newly appearing IP.
- Stop with `Ctrl+C` after locating the target.
- Confirm the IP by browsing or scanning it before deeper testing.
- False positive: DHCP changes can make an unrelated device look new.
- Edge case: ARP discovery works only on the local Layer-2 network.
- Remediation note: lab-only discovery technique; production networks should segment sensitive hosts.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 5
