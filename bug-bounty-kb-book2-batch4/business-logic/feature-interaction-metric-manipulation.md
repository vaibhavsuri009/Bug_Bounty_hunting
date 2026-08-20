# Feature-Interaction Metric Manipulation

- What it is: Two individually valid features interact to produce an unintended business-logic result.
- Identify newly launched metrics, quotas, scores, or reputation calculations.
- Map every event that feeds the calculation, including rare states such as self-close/retract.
- Create controlled records in each state and observe how the aggregate metric changes.
- The HackerOne Signal example let self-closed zero-value reports improve a negative average.
- Focus on edge states developers may have omitted from the model.
- False positive: a surprising metric may still match documented product rules.
- Edge case: asynchronous recalculation can delay evidence.
- Remediation: explicitly define excluded states and test cross-feature invariants.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
