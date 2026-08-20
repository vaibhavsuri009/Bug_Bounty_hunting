# Rails Mass Assignment

- What it is: The backend accepts attacker-supplied model fields that the UI never intended users to modify.
- Look for create/update endpoints on older Rails or custom parameter-binding code.
- Add extra model attributes to a legitimate request one at a time.
- Candidate fields include role, owner/admin flags, creation dates, IDs, or permission fields.
- Confirm whether the server persists fields absent from the UI.
- The book describes historical Rails defaults that accepted all controller parameters.
- False positive: a field echoed back but ignored by persistence is not mass assignment.
- Edge case: framework protections may exist but individual code paths can explicitly bypass them.
- Remediation: allowlist permitted fields/strong parameters for every update/create action.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
