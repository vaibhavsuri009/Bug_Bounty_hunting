# CDN and Cache Security Mapping

- What it is: CDNs and browser/network caches introduce additional copies of application data outside the origin server.
- Where to look / how to identify it:
  - Record CDN hosts, cache headers, browser storage, and which resources appear cacheable.
- Exploitation / test pattern:
  - Check whether user-specific or privileged responses are cached where another user could receive them.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Network headers: `Cache-Control`, `ETag`, CDN-related hosts.
- Common false-positive / WAF / edge-case notes:
  - A cached static asset is normal; focus on private or user-specific data.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use correct cache-control directives, vary keys on authorization context, and avoid shared caching of sensitive responses.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
