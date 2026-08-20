# Arjun Hidden Parameter Discovery

- What it is: Arjun discovers undocumented HTTP parameters using a large parameter dictionary and anomaly detection.
- Install under `/opt`:
```bash
cd /opt/
sudo git clone https://github.com/s0med3v/Arjun.git
```
- Scan one endpoint:
```bash
python3 /opt/Arjun/arjun.py -u http://target_address.com
```
- Save JSON with `-o arjun_results.json`; use `-i <file>` for multiple targets.
- Add `--stable` when the target cannot handle the default request pattern.
- False positive: response anomalies may come from rate limiting or application instability.
- Remediation: reject unknown parameters and explicitly bind accepted request fields.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
