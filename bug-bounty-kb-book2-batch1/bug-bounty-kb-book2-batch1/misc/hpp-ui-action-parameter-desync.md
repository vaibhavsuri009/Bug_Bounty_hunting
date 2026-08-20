# HPP UI / Action Parameter Desynchronization

- What it is: Duplicate parameters can make the confirmation UI describe one object while the submitted action targets another.
- Where to look: Confirmation pages, follow/like/share dialogs, checkout screens, and multi-step actions.
- Duplicate an object-identifying parameter with two different values.
- Example pattern:
```text
/intent/follow?screen_name=trusted&screen_name=attacker
```
- Compare the object shown in the UI with hidden form fields and the form `action` destination.
- Submit only with test accounts and verify whether the backend acts on a different value from the one displayed.
- Also try injecting parameters that are meaningful to the generated form but absent from the original workflow.
- False-positive trap: Different HTML representations are not exploitable unless the final state-changing request is affected.
- Remediation: Derive display and action data from one canonical, server-validated parameter set.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 3
