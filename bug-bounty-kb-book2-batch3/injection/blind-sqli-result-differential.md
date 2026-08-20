# Blind SQLi via Result Differential

- What it is: SQL executes but direct query output is hidden, so response differences become the oracle.
- Capture a stable baseline request first.
- Modify a numeric parameter with SQL comment syntax and compare page content.
```text
year=2010
year=2010--
```
- Look for changed rows, counts, page sections, or empty results.
- Follow with paired true/false Boolean conditions to reduce ambiguity.
- The Yahoo example inferred SQLi from subtle changes in returned player lists.
- False positive: normal application branching can also change results.
- Edge case: caching can mask or exaggerate differences; repeat requests.
- Remediation: prepared statements and consistent server-side parameter validation.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
