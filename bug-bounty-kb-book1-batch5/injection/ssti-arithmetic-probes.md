# SSTI Arithmetic Probes

- Arithmetic probes confirm that input is evaluated as template code instead of rendered literally.
- Payloads given in the chapter:
```text
${7*7}
{{7*7}}
<%= 7*7 %>
```
- A returned value of `49` indicates the relevant syntax was evaluated.
- If user input is already placed inside template expression delimiters, try just:
```text
7*7
```
- Check delayed destinations such as emails or generated files when immediate output is absent.
- False-positive trap: a literal `49` already present in the response is not evidence; correlate it to your exact injection point.
- Remediation: treat untrusted values as data and keep template syntax under developer control.
## Source: Bug Bounty Bootcamp, Ch. 16
