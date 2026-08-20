# IndexedDB Recon

- What it is: IndexedDB is a browser-side asynchronous NoSQL database used by complex web applications to persist structured data.
- Where to look / how to identify it:
  - Check for IndexedDB databases, object stores, cached objects, offline data, and tokens using DevTools.
- Exploitation / test pattern:
  - Map any sensitive client-side datasets and determine whether they are needed for application functionality.
- Tools + exact CLI syntax (if mentioned):
  - Console detection: `if (window.indexedDB) { console.log('true'); }`
- Common false-positive / WAF / edge-case notes:
  - Large client-side datasets are not inherently unsafe when only public/non-sensitive data is stored.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Minimize sensitive offline data and encrypt or avoid storing reusable secrets.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
