# AngularJS CSTI Probe and Version Check

- What it is: User input is evaluated as an AngularJS template expression in the browser.
- Look for AngularJS markers such as `ng-` attributes or framework detection results.
- Submit a benign expression into reflected fields/parameters.
```text
{{7*7}}
```
- Rendering `49` indicates Angular expression evaluation.
- Determine the AngularJS version in the browser developer console.
```javascript
Angular.version
```
- The book notes that older pre-1.6 releases used a Sandbox that changed exploitation requirements.
- False positive: arithmetic evaluation alone may be non-exploitable if character/length restrictions block JavaScript.
- Edge case: test restrictions such as removed `*`, `()`, `[]`, or strict maximum input length.
- Remediation: update AngularJS and prevent untrusted text from entering template-expression contexts.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 8
