# SendGrid Inbound Parse Domain Takeover

- What it is: A domain already points MX records to SendGrid but is not bound to an account's Inbound Parse Webhook.
- Review target MX/CNAME records pointing to SendGrid.
- Read provider documentation for alternate services that reuse the same DNS prerequisites.
- The historical flow required an MX to `mx.sendgrid.net` plus an account-side parse-domain association.
- If the second binding is missing, the domain may historically have been claimable.
- Do not intercept real email; stop after minimal ownership proof if authorized.
- False positive: SendGrid now performs additional domain verification, so the historical issue may not apply.
- Edge case: mail-routing takeover impact differs from web-content takeover.
- Remediation: require domain ownership verification for every service binding.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 14
