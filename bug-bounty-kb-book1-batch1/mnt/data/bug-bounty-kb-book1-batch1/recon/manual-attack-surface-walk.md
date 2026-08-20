# Manual Attack-Surface Walkthrough

- What it is: Systematically use every reachable feature to map the application's attack surface before deeper testing.
- Browse every page and follow every visible link.
- Exercise rarely used functions, not only the primary workflow.
- Create accounts at each available privilege level.
- If the application supports groups/channels/tenants, create users in different memberships.
- Record how each role sees and uses the same features.
- Identify all data-entry points and state-changing actions.
- Note how users interact with one another and which objects cross privilege boundaries.
- Capture interesting requests in Burp while walking the application.
- Record hidden-looking endpoints, unusual parameters, and privilege-dependent functionality.
- Edge case: some functionality appears only after specific account state, role, or workflow transitions.
- Remediation: N/A — reconnaissance methodology.

## Source: Bug Bounty Bootcamp, Ch. 5
