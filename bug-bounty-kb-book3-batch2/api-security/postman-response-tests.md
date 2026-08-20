# Postman Response Tests

- What it is: Postman can automatically assert response status, timing, and content.
- Add JavaScript tests in the Tests panel.
```javascript
pm.test("Status code is 200", function () {
  pm.response.to.have.status(200);
});
```
- Adapt the expected code/body/timing to the endpoint under test.
- Validate the test itself by creating both passing and failing conditions.
- Use results during collection runs to surface anomalies quickly.
- False positive: a `200` can still contain an application-level error.
- Edge case: dynamic response bodies require targeted assertions rather than exact matches.
- Remediation note: server-side tests should cover the same security expectations continuously.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
