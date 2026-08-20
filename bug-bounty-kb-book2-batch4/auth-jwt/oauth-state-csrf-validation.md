# OAuth `state` CSRF Validation

- What it is: Missing or weak `state` binding can let an attacker initiate/complete OAuth in another user's browser.
- Capture a legitimate OAuth authorization request and callback.
- Remove, reuse, or alter the `state` parameter.
- Check whether the client still accepts the callback.
- `state` should be unguessable, session-bound, and validated on return.
- Test with two controlled browser sessions to detect cross-session reuse.
- False positive: a framework may use an equivalent anti-CSRF mechanism outside the visible `state`.
- Edge case: state values that are signed but not session-bound may still be replayable.
- Remediation: generate high-entropy per-flow state and bind it to the initiating user session.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 17
