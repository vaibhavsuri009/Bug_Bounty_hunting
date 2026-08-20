# Email Change vs Verification Race

- What it is: A verification token for one email is accepted after the account email is changed to another address.
- Create an account with an email you control and request verification.
- Intercept the email-change request and the original verification request.
- Send the change and verification requests almost simultaneously.
- Verify whether the application marks the new, unowned email as verified.
- The Shopify example used Burp to race these two requests.
- False positive: a UI "verified" label is insufficient if privileged workflows still revalidate ownership.
- Edge case: downstream authorization may amplify impact through identity-based account matching.
- Remediation: bind verification tokens to the exact email value and lock the account record during changes.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 15
