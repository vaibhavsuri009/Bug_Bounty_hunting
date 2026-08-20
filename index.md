# index.md — 4-Book Web Security Knowledge Base

**Total technique files:** 848

This is the master index for all four processed books. It links to the consolidated technique notes.

## Books

1. **Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities** — Vickie Li — **243 techniques**
2. **Real-World Bug Hunting — A Field Guide to Web Hacking** — Peter Yaworski — **150 techniques**
3. **Hacking APIs — Breaking Web Application Programming Interfaces** — Corey J. Ball — **164 techniques**
4. **Web Application Security, 2nd Edition** — Andrew Hoffman — **291 techniques**

## Quick Counts

| Book | Technique files |
|---|---:|
| 1 | 243 |
| 2 | 150 |
| 3 | 164 |
| 4 | 291 |
| **Total** | **848** |

## Complete Index

## Book 1 — Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities

**Author:** Vickie Li

### By Category

#### IDOR / Object Authorization

- [Blind IDOR](book1/idor/blind-idor.md) — Ch. 10 — Batch 4
- [Encoded ID Bypass](book1/idor/encoded-id-bypass.md) — Ch. 10 — Batch 4
- [File Reference IDOR](book1/idor/file-reference-idor.md) — Ch. 10 — Batch 4
- [Hidden ID Parameter Injection](book1/idor/hidden-id-parameter-injection.md) — Ch. 10 — Batch 4
- [IDOR Authorization Automation with Burp](book1/idor/authorization-automation-burp.md) — Ch. 10 — Batch 4
- [IDOR File Extension Bypass](book1/idor/file-extension-bypass.md) — Ch. 10 — Batch 4
- [IDOR HTTP Method Switch Bypass](book1/idor/http-method-switch-bypass.md) — Ch. 10 — Batch 4
- [Leaked ID Chaining](book1/idor/leaked-id-chaining.md) — Ch. 10 — Batch 4
- [Numeric ID Swap IDOR](book1/idor/numeric-id-swap.md) — Ch. 10 — Batch 4
- [Predictable Randomized ID Analysis](book1/idor/predictable-randomized-id-analysis.md) — Ch. 10 — Batch 4
- [Two-Account Authorization Testing](book1/idor/two-account-authorization-testing.md) — Ch. 10 — Batch 4

#### Injection

- [Boolean-Based Blind SQL Injection](book1/injection/blind-sql-boolean.md) — Ch. 11 — Batch 4
- [Error-Based SQL Injection](book1/injection/sql-error-based.md) — Ch. 11 — Batch 4
- [MongoDB `$ne` Authentication Bypass](book1/injection/nosql-mongodb-ne-auth-bypass.md) — Ch. 11 — Batch 4
- [NoSQL Injection Probing](book1/injection/nosql-injection-probing.md) — Ch. 11 — Batch 4
- [Second-Order SQL Injection](book1/injection/second-order-sql-injection.md) — Ch. 11 — Batch 4
- [SQL Database Fingerprinting](book1/injection/sql-database-fingerprinting.md) — Ch. 11 — Batch 4
- [SQL Injection Authentication Bypass with Comments](book1/injection/sql-auth-bypass-comment.md) — Ch. 11 — Batch 4
- [SQL Injection Automation with sqlmap](book1/injection/sqlmap-automation.md) — Ch. 11 — Batch 4
- [SQL Injection OUTFILE Exfiltration](book1/injection/sql-outfile-exfiltration.md) — Ch. 11 — Batch 4
- [SQL Injection Single-Quote Probe](book1/injection/sql-single-quote-probe.md) — Ch. 11 — Batch 4
- [SQL Injection to Web Shell via OUTFILE](book1/injection/sql-web-shell-outfile.md) — Ch. 11 — Batch 4
- [SQL Schema Enumeration](book1/injection/sql-schema-enumeration.md) — Ch. 11 — Batch 4
- [Time-Based Blind SQL Injection](book1/injection/blind-sql-time.md) — Ch. 11 — Batch 4
- [UNION-Based SQL Injection](book1/injection/sql-union-based.md) — Ch. 11 — Batch 4

#### Miscellaneous

- [Burp Browser + Proxy Setup](book1/misc/burp-proxy-browser-setup.md) — Ch. 4 — Batch 1
- [Burp Comparer Response Diffing](book1/misc/burp-comparer-response-diffing.md) — Ch. 4 — Batch 1
- [Burp Decoder for Encoded Application Data](book1/misc/burp-decoder-encoded-data.md) — Ch. 4 — Batch 1
- [Burp HTTPS Interception](book1/misc/burp-https-interception.md) — Ch. 4 — Batch 1
- [Burp Intruder Request Fuzzing](book1/misc/burp-intruder-request-fuzzing.md) — Ch. 4 — Batch 1
- [Burp Proxy Request Tampering](book1/misc/burp-proxy-request-tampering.md) — Ch. 4 — Batch 1
- [Burp Repeater Manual Request Testing](book1/misc/burp-repeater-manual-testing.md) — Ch. 4 — Batch 1
- [Save Burp Requests as Reproducible Artifacts](book1/misc/save-burp-request-as-curl.md) — Ch. 4 — Batch 1
- [Open Redirect Browser Autocorrect Bypass](book1/open-redirect-browser-autocorrect-bypass.md) — Ch. 7 — Batch 3
- [Open Redirect Bypass Chaining](book1/open-redirect-bypass-chaining.md) — Ch. 7 — Batch 3
- [Open Redirect Data URL Bypass](book1/open-redirect-data-url-bypass.md) — Ch. 7 — Batch 3
- [Open Redirect Double-Encoding Bypass](book1/open-redirect-double-encoding-bypass.md) — Ch. 7 — Batch 3
- [Open Redirect Google Dorks](book1/open-redirect-google-dorks.md) — Ch. 7 — Batch 3
- [Open Redirect Parameter Discovery](book1/open-redirect-parameter-discovery.md) — Ch. 7 — Batch 3
- [Open Redirect Security Impact Chaining](book1/open-redirect-security-impact.md) — Ch. 7 — Batch 3
- [Open Redirect Unicode Normalization Bypass](book1/open-redirect-unicode-normalization-bypass.md) — Ch. 7 — Batch 3
- [Open Redirect Validator Logic Bypass](book1/open-redirect-validator-logic-bypass.md) — Ch. 7 — Batch 3
- [Parameter-Based Open Redirect Test](book1/open-redirect-parameter-test.md) — Ch. 7 — Batch 3
- [Referer-Based Open Redirect](book1/referer-based-open-redirect.md) — Ch. 7 — Batch 3
- [Clickjacking Double-Iframe Frame-Busting Bypass](book1/clickjacking-double-iframe-bypass.md) — Ch. 8 — Batch 3
- [Clickjacking Frameability Test](book1/clickjacking-frameability-test.md) — Ch. 8 — Batch 3
- [Clickjacking Impact Chaining](book1/clickjacking-impact-chaining.md) — Ch. 8 — Batch 3
- [Clickjacking Overlay PoC](book1/clickjacking-overlay-poc.md) — Ch. 8 — Batch 3
- [Clickjacking Protection Audit](book1/clickjacking-protection-audit.md) — Ch. 8 — Batch 3
- [CSRF + Self-XSS to Stored XSS](book1/csrf-self-xss-chain.md) — Ch. 9 — Batch 3
- [CSRF Account-Takeover Chain](book1/csrf-account-takeover-chain.md) — Ch. 9 — Batch 3
- [CSRF Auto-Submitting HTML Form PoC](book1/csrf-html-form-poc.md) — Ch. 9 — Batch 3
- [CSRF Cross-Session Token Bypass](book1/csrf-cross-session-token-bypass.md) — Ch. 9 — Batch 3
- [CSRF Double-Submit Cookie Bypass](book1/csrf-double-submit-cookie-bypass.md) — Ch. 9 — Batch 3
- [CSRF Missing or Blank Token Bypass](book1/csrf-missing-blank-token-bypass.md) — Ch. 9 — Batch 3
- [CSRF Protection Bypass via XSS](book1/csrf-xss-chain.md) — Ch. 9 — Batch 3
- [CSRF Referer-Header Bypass](book1/csrf-referer-header-bypass.md) — Ch. 9 — Batch 3
- [CSRF Request-Method Switch Bypass](book1/csrf-method-switch-bypass.md) — Ch. 9 — Batch 3
- [CSRF State-Changing Request Discovery](book1/csrf-state-changing-request-discovery.md) — Ch. 9 — Batch 3
- [CSRF to Information Disclosure Chain](book1/csrf-info-leak-chain.md) — Ch. 9 — Batch 3
- [CSRF via Clickjacking Chain](book1/csrf-clickjacking-chain.md) — Ch. 9 — Batch 3
- [Blind SSRF OOB Detection](book1/blind-ssrf-oob-detection.md) — Ch. 13 — Batch 5
- [Blind SSRF Port Scanning](book1/blind-ssrf-port-scanning.md) — Ch. 13 — Batch 5
- [SSRF Allowlist Bypass via Open Redirect](book1/ssrf-allowlist-open-redirect-bypass.md) — Ch. 13 — Batch 5
- [SSRF AWS Instance Metadata Access](book1/ssrf-aws-instance-metadata.md) — Ch. 13 — Batch 5
- [SSRF Blocklist Bypass via Redirect](book1/ssrf-blocklist-redirect-bypass.md) — Ch. 13 — Batch 5
- [SSRF DNS Resolution Bypass](book1/ssrf-dns-resolution-bypass.md) — Ch. 13 — Batch 5
- [SSRF Entry-Point Discovery](book1/ssrf-entry-point-discovery.md) — Ch. 13 — Batch 5
- [SSRF Google Cloud Metadata Access](book1/ssrf-google-cloud-metadata.md) — Ch. 13 — Batch 5
- [SSRF Internal API Access](book1/ssrf-internal-api-access.md) — Ch. 13 — Batch 5
- [SSRF Internal Network Scanning](book1/ssrf-internal-network-scanning.md) — Ch. 13 — Batch 5
- [SSRF Internal Port Scanning](book1/ssrf-internal-port-scanning.md) — Ch. 13 — Batch 5
- [SSRF Internal URL Probing](book1/ssrf-internal-url-probing.md) — Ch. 13 — Batch 5
- [SSRF IP Encoding Bypass](book1/ssrf-ip-encoding-bypass.md) — Ch. 13 — Batch 5
- [SSRF IPv6 Blocklist Bypass](book1/ssrf-ipv6-bypass.md) — Ch. 13 — Batch 5
- [SSRF Regex Allowlist Bypass](book1/ssrf-allowlist-regex-bypass.md) — Ch. 13 — Batch 5
- [Insecure Deserialization Hunting](book1/deserialization-hunting.md) — Ch. 14 — Batch 5
- [Java Deserialization Gadget Chains](book1/java-deserialization-gadget-chain.md) — Ch. 14 — Batch 5
- [Java Serialized Object Recognition](book1/java-serialized-object-recognition.md) — Ch. 14 — Batch 5
- [Java Serialized Object Tampering](book1/java-serialized-object-tampering.md) — Ch. 14 — Batch 5
- [PHP Magic-Method Deserialization RCE](book1/php-magic-method-rce.md) — Ch. 14 — Batch 5
- [PHP POP-Chain Deserialization](book1/php-pop-chain-rce.md) — Ch. 14 — Batch 5
- [PHP Serialized Object Recognition](book1/php-serialized-object-recognition.md) — Ch. 14 — Batch 5
- [PHP Serialized Property Tampering](book1/php-object-property-tampering.md) — Ch. 14 — Batch 5
- [Ysoserial Java Deserialization Payloads](book1/ysoserial-java-deserialization.md) — Ch. 14 — Batch 5
- [Blind XXE Error-Based Exfiltration](book1/blind-xxe-error-exfiltration.md) — Ch. 15 — Batch 5
- [Blind XXE External-DTD Exfiltration](book1/blind-xxe-external-dtd-exfiltration.md) — Ch. 15 — Batch 5
- [Blind XXE OOB Detection](book1/blind-xxe-oob-detection.md) — Ch. 15 — Batch 5
- [Classic XXE File Read](book1/classic-xxe-file-read.md) — Ch. 15 — Batch 5
- [XInclude File Read](book1/xinclude-file-read.md) — Ch. 15 — Batch 5
- [XXE Billion-Laughs / XML Bomb](book1/xxe-billion-laughs-dos.md) — Ch. 15 — Batch 5
- [XXE CDATA Exfiltration](book1/xxe-cdata-exfiltration.md) — Ch. 15 — Batch 5
- [XXE Entry-Point Discovery](book1/xxe-entry-point-discovery.md) — Ch. 15 — Batch 5
- [XXE FTP Exfiltration](book1/xxe-ftp-exfiltration.md) — Ch. 15 — Batch 5
- [XXE in Office Document Archives](book1/xxe-office-document-smuggling.md) — Ch. 15 — Batch 5
- [XXE PHP-Filter Base64 Exfiltration](book1/xxe-php-filter-base64-exfiltration.md) — Ch. 15 — Batch 5
- [XXE via SVG Upload](book1/xxe-svg-upload.md) — Ch. 15 — Batch 5
- [XXE-to-SSRF](book1/xxe-ssrf.md) — Ch. 15 — Batch 5
- [Jinja2 `catch_warnings` Sandbox Escape](book1/jinja2-catch-warnings-sandbox-escape.md) — Ch. 16 — Batch 5
- [Jinja2 Command-Execution PoC](book1/jinja2-command-execution-poc.md) — Ch. 16 — Batch 5
- [Jinja2 Sandbox Class Enumeration](book1/jinja2-sandbox-class-enumeration.md) — Ch. 16 — Batch 5
- [SSTI Arithmetic Probes](book1/ssti-arithmetic-probes.md) — Ch. 16 — Batch 5
- [SSTI Automation with Tplmap](book1/ssti-tplmap-automation.md) — Ch. 16 — Batch 5
- [SSTI Error-Probe Detection](book1/ssti-error-probe.md) — Ch. 16 — Batch 5
- [SSTI Input-Point Discovery](book1/ssti-input-discovery.md) — Ch. 16 — Batch 5
- [SSTI Template-Engine Fingerprinting](book1/ssti-engine-fingerprinting.md) — Ch. 16 — Batch 5
- [Cookie-Based Access-Control Bypass](book1/cookie-based-access-control-bypass.md) — Ch. 17 — Batch 6
- [Directory Traversal via Filepath Input](book1/directory-traversal-basic.md) — Ch. 17 — Batch 6
- [Exposed Admin Panel Discovery](book1/exposed-admin-panel-discovery.md) — Ch. 17 — Batch 6
- [Forced Browsing Access-Control Bypass](book1/forced-browsing-access-control-bypass.md) — Ch. 17 — Batch 6
- [Payment Verification Parameter Bypass](book1/payment-verification-parameter-bypass.md) — Ch. 17 — Batch 6
- [Skippable Authentication Step](book1/skippable-authentication-step.md) — Ch. 17 — Batch 6
- [Blind RCE Out-of-Band Confirmation](book1/rce-oob-callback.md) — Ch. 18 — Batch 6
- [Blind RCE via Time Delay](book1/blind-rce-time-delay.md) — Ch. 18 — Batch 6
- [Classic RCE Verification](book1/classic-rce-verification.md) — Ch. 18 — Batch 6
- [Duplicate-Parameter RCE Filter Bypass](book1/http-parameter-splitting-rce-bypass.md) — Ch. 18 — Batch 6
- [Local File Inclusion (LFI) via Uploaded File](book1/local-file-inclusion.md) — Ch. 18 — Batch 6
- [PHP Code-Execution Filter Bypass](book1/php-rce-filter-bypass.md) — Ch. 18 — Batch 6
- [Python Code-Execution Filter Bypass](book1/python-rce-filter-bypass.md) — Ch. 18 — Batch 6
- [Python eval() Code Injection](book1/python-eval-code-injection.md) — Ch. 18 — Batch 6
- [Remote File Inclusion (RFI)](book1/remote-file-inclusion.md) — Ch. 18 — Batch 6
- [Safe RCE Proof of Concept](book1/rce-safe-proof-of-concept.md) — Ch. 18 — Batch 6
- [Shell Command Injection](book1/shell-command-injection.md) — Ch. 18 — Batch 6
- [Unix Command Filter Bypass](book1/unix-command-filter-bypass.md) — Ch. 18 — Batch 6
- [CORS Arbitrary Origin Reflection](book1/cors-arbitrary-origin-reflection.md) — Ch. 19 — Batch 6
- [CORS null-Origin Misconfiguration](book1/cors-null-origin.md) — Ch. 19 — Batch 6
- [CORS Weak Regex Origin Bypass](book1/cors-regex-origin-bypass.md) — Ch. 19 — Batch 6
- [JSONP Sensitive Data Exposure](book1/jsonp-sensitive-data-exposure.md) — Ch. 19 — Batch 6
- [postMessage Missing Sender-Origin Validation](book1/postmessage-missing-sender-validation.md) — Ch. 19 — Batch 6
- [postMessage Wildcard Target-Origin Leak](book1/postmessage-wildcard-target-origin.md) — Ch. 19 — Batch 6
- [SOP Relaxation Fingerprinting](book1/sop-relaxation-fingerprinting.md) — Ch. 19 — Batch 6
- [Continuous Subdomain Takeover Monitoring](book1/subdomain-takeover-monitoring.md) — Ch. 20 — Batch 6
- [Dangling CNAME Subdomain Takeover](book1/subdomain-takeover-dangling-cname.md) — Ch. 20 — Batch 6
- [OAuth Token Lifetime / Revocation Test](book1/oauth-token-lifetime-test.md) — Ch. 20 — Batch 6
- [OAuth Token Theft via Open Redirect](book1/oauth-open-redirect-token-theft.md) — Ch. 20 — Batch 6
- [OAuth Token Theft via Redirect Chain](book1/oauth-open-redirect-chain.md) — Ch. 20 — Batch 6
- [SAML Empty/Removed Signature Bypass](book1/saml-empty-signature-bypass.md) — Ch. 20 — Batch 6
- [SAML Predictable Signature Forgery](book1/saml-predictable-signature-forgery.md) — Ch. 20 — Batch 6
- [SAML Response Editing and Re-encoding](book1/saml-raider-edit-reencode.md) — Ch. 20 — Batch 6
- [SAML Unsigned Assertion Tampering](book1/saml-unsigned-assertion-tampering.md) — Ch. 20 — Batch 6
- [Shared-Cookie + Subdomain Takeover Chain](book1/shared-cookie-subdomain-takeover-chain.md) — Ch. 20 — Batch 6
- [SSO Mechanism Fingerprinting](book1/sso-mechanism-fingerprinting.md) — Ch. 20 — Batch 6
- [Decompress Exposed Git Objects](book1/git-object-decompression.md) — Ch. 21 — Batch 6
- [Exposed .git Directory Detection](book1/exposed-git-directory-detection.md) — Ch. 21 — Batch 6
- [Manual .git Reconstruction](book1/exposed-git-manual-reconstruction.md) — Ch. 21 — Batch 6
- [Paste Dump Secret Search](book1/paste-dump-secret-search.md) — Ch. 21 — Batch 6
- [Path Traversal Encoding Bypass](book1/path-traversal-encoding-bypass.md) — Ch. 21 — Batch 6
- [Public JavaScript Secret Hunting](book1/public-js-secret-hunting.md) — Ch. 21 — Batch 6
- [Recursive Download of Exposed .git](book1/exposed-git-recursive-download.md) — Ch. 21 — Batch 6
- [Software Version Disclosure](book1/software-version-disclosure.md) — Ch. 21 — Batch 6
- [Wayback Sensitive File Discovery](book1/wayback-sensitive-file-discovery.md) — Ch. 21 — Batch 6
- [Code Review: Developer Comments and Debug Endpoints](book1/code-review-comments-debug-endpoints.md) — Ch. 22 — Batch 7
- [Code Review: Grep for Dangerous Sinks](book1/code-review-dangerous-sinks-grep.md) — Ch. 22 — Batch 7
- [Code Review: Hardcoded Secret Hunting](book1/code-review-secret-grep.md) — Ch. 22 — Batch 7
- [Code Review: Incomplete CSRF Validation](book1/code-review-csrf-bypass-review.md) — Ch. 22 — Batch 7
- [Code Review: One Input, Multiple Vulnerable Sinks](book1/code-review-multi-sink-input-tracing.md) — Ch. 22 — Batch 7
- [Code Review: Outdated Dependency Review](book1/code-review-dependency-cve-review.md) — Ch. 22 — Batch 7
- [Code Review: Trace Security-Critical Functions](book1/code-review-sensitive-flow-tracing.md) — Ch. 22 — Batch 7
- [Code Review: User-Input Taint Tracing](book1/code-review-user-input-taint-tracing.md) — Ch. 22 — Batch 7
- [Code Review: Weak Cryptography Search](book1/code-review-weak-crypto-grep.md) — Ch. 22 — Batch 7
- [Code Review: Weak Redirect Validation](book1/code-review-open-redirect-validation-review.md) — Ch. 22 — Batch 7
- [SAST-Assisted Source Code Review](book1/sast-assisted-code-review.md) — Ch. 22 — Batch 7
- [Android: ADB Device and File Workflow](book1/android-adb-basics.md) — Ch. 23 — Batch 7
- [Android: APK and AndroidManifest Recon](book1/android-apk-manifest-recon.md) — Ch. 23 — Batch 7
- [Android: Apktool Decompile and Rebuild](book1/android-apktool-decompile-rebuild.md) — Ch. 23 — Batch 7
- [Android: Bypass Certificate Pinning with Frida/Objection](book1/android-cert-pinning-objection-frida.md) — Ch. 23 — Batch 7
- [Android: Compare Mobile vs Web Authorization](book1/android-mobile-web-auth-diff-testing.md) — Ch. 23 — Batch 7
- [Android: Frida Runtime Instrumentation](book1/android-frida-runtime-analysis.md) — Ch. 23 — Batch 7
- [Android: Hunt Hardcoded Secrets in APK Resources](book1/android-hardcoded-secret-hunting.md) — Ch. 23 — Batch 7
- [Android: Install Burp CA for HTTPS Interception](book1/android-burp-ca-install.md) — Ch. 23 — Batch 7
- [Android: MobSF Static and Dynamic Triage](book1/android-mobsf-static-dynamic-analysis.md) — Ch. 23 — Batch 7
- [Android: Review Bundled SQLite/DB Files](book1/android-sqlite-sensitive-data-review.md) — Ch. 23 — Batch 7
- [Android: Route App Traffic Through Burp](book1/android-burp-proxy-setup.md) — Ch. 23 — Batch 7
- [API Recon: Capture Workflows and Deduce Hidden Endpoints](book1/api-workflow-capture-endpoint-deduction.md) — Ch. 24 — Batch 7
- [API Recon: Public and Exposed Swagger Documentation](book1/api-documentation-swagger-recon.md) — Ch. 24 — Batch 7
- [API Recon: Test Older API Versions](book1/api-version-downgrade-testing.md) — Ch. 24 — Batch 7
- [API: Access-Token Lifecycle Testing](book1/api-token-lifecycle-testing.md) — Ch. 24 — Batch 7
- [API: BOLA/IDOR Testing](book1/api-bola-idor-testing.md) — Ch. 24 — Batch 7
- [API: Excessive Data Exposure](book1/api-excessive-data-exposure.md) — Ch. 24 — Batch 7
- [API: HTTP Method Authorization Bypass](book1/api-method-access-control-bypass.md) — Ch. 24 — Batch 7
- [API: Rate-Limit Testing](book1/api-rate-limit-testing.md) — Ch. 24 — Batch 7
- [API: Re-test Web Injection Classes Through API Inputs](book1/api-technical-injection-surface.md) — Ch. 24 — Batch 7
- [GraphQL: Endpoint Discovery](book1/graphql-endpoint-discovery.md) — Ch. 24 — Batch 7
- [GraphQL: Enumerate Fields with __type](book1/graphql-type-field-enum.md) — Ch. 24 — Batch 7
- [GraphQL: Enumerate Types with Introspection](book1/graphql-introspection-schema-enum.md) — Ch. 24 — Batch 7
- [GraphQL: Mutation Authorization Testing](book1/graphql-mutation-authorization-testing.md) — Ch. 24 — Batch 7
- [GraphQL: Recon When Introspection Is Disabled](book1/graphql-introspection-disabled-recon.md) — Ch. 24 — Batch 7
- [SOAP: WSDL Endpoint Discovery](book1/soap-wsdl-discovery.md) — Ch. 24 — Batch 7
- [Burp Intruder: Fuzzing Workflow](book1/burp-intruder-fuzzing-workflow.md) — Ch. 25 — Batch 7
- [Fuzzing: Map Data Injection Points](book1/fuzzing-injection-point-mapping.md) — Ch. 25 — Batch 7
- [Fuzzing: Payload List Strategy](book1/fuzzing-payload-list-strategy.md) — Ch. 25 — Batch 7
- [Fuzzing: Triage Response Anomalies](book1/fuzzing-response-anomaly-triage.md) — Ch. 25 — Batch 7
- [Wfuzz: Basic Authentication Fuzzing](book1/wfuzz-basic-auth-bruteforce.md) — Ch. 25 — Batch 7
- [Wfuzz: IDOR/BOLA Enumeration](book1/wfuzz-idor-fuzzing.md) — Ch. 25 — Batch 7
- [Wfuzz: Open Redirect Fuzzing](book1/wfuzz-open-redirect-fuzzing.md) — Ch. 25 — Batch 7
- [Wfuzz: Path Enumeration](book1/wfuzz-path-enumeration.md) — Ch. 25 — Batch 7
- [Wfuzz: Reflected XSS Fuzzing](book1/wfuzz-reflected-xss-fuzzing.md) — Ch. 25 — Batch 7
- [Wfuzz: SQL Injection Fuzzing](book1/wfuzz-sqli-fuzzing.md) — Ch. 25 — Batch 7

#### Race Conditions

- [Race Condition Remediation with Resource Locking](book1/race-conditions/resource-locking-remediation.md) — Ch. 12 — Batch 4
- [Race Condition Result Validation](book1/race-conditions/race-condition-result-validation.md) — Ch. 12 — Batch 4
- [Race Condition Target Selection](book1/race-conditions/race-condition-target-selection.md) — Ch. 12 — Batch 4
- [Simultaneous Requests with `curl`](book1/race-conditions/simultaneous-curl-requests.md) — Ch. 12 — Batch 4
- [TOCTOU Race Condition](book1/race-conditions/toctou-race-condition.md) — Ch. 12 — Batch 4

#### Reconnaissance

- [Bash Recon Wrapper](book1/recon/bash-recon-wrapper.md) — Ch. 5 — Batch 2
- [Building a Master Recon Report](book1/recon/master-recon-report.md) — Ch. 5 — Batch 2
- [Certificate SAN Host Enumeration](book1/recon/certificate-san-enumeration.md) — Ch. 5 — Batch 1
- [crt.sh JSON Automation](book1/recon/crtsh-json-automation.md) — Ch. 5 — Batch 2
- [Diff-Based Attack-Surface Monitoring](book1/recon/diff-based-attack-surface-monitoring.md) — Ch. 5 — Batch 2
- [Directory and File Brute-Forcing](book1/recon/directory-bruteforce.md) — Ch. 5 — Batch 1
- [GitHub Secret and Source Recon](book1/recon/github-secret-recon.md) — Ch. 5 — Batch 1
- [Google Dorking for Target Recon](book1/recon/google-dorking.md) — Ch. 5 — Batch 1
- [Interactive Recon Loop](book1/recon/interactive-recon-loop.md) — Ch. 5 — Batch 2
- [IP Range and ASN Discovery](book1/recon/ip-range-asn-discovery.md) — Ch. 5 — Batch 1
- [Manual Attack-Surface Walkthrough](book1/recon/manual-attack-surface-walk.md) — Ch. 5 — Batch 1
- [Multi-Domain Recon with getopts](book1/recon/multi-domain-getopts-recon.md) — Ch. 5 — Batch 2
- [OSINT for Technology and Internal Clues](book1/recon/osint-tech-stack-leaks.md) — Ch. 5 — Batch 1
- [Parsing Nmap Output with grep](book1/recon/grep-nmap-results.md) — Ch. 5 — Batch 2
- [Reusable Recon Function Library](book1/recon/reusable-recon-functions.md) — Ch. 5 — Batch 2
- [S3 Bucket Discovery and Access Testing](book1/recon/s3-bucket-recon.md) — Ch. 5 — Batch 1
- [Saving Recon Output with Redirection](book1/recon/recon-output-redirection.md) — Ch. 5 — Batch 2
- [Scheduled Continuous Recon with cron](book1/recon/cron-continuous-recon.md) — Ch. 5 — Batch 2
- [Selective Recon Scan Modes](book1/recon/recon-scan-modes.md) — Ch. 5 — Batch 2
- [Service Enumeration](book1/recon/service-enumeration.md) — Ch. 5 — Batch 1
- [Subdomain Enumeration](book1/recon/subdomain-enumeration.md) — Ch. 5 — Batch 1
- [Technology Stack Fingerprinting](book1/recon/tech-stack-fingerprinting.md) — Ch. 5 — Batch 1
- [Wayback Endpoint Discovery](book1/recon/wayback-endpoint-discovery.md) — Ch. 5 — Batch 1
- [Web Spidering / Crawling](book1/recon/web-spidering.md) — Ch. 5 — Batch 1
- [WHOIS and Reverse-WHOIS Scope Discovery](book1/recon/whois-reverse-whois.md) — Ch. 5 — Batch 1

#### XSS

- [Blind XSS](book1/xss/blind-xss.md) — Ch. 6 — Batch 2
- [DOM-Based XSS](book1/xss/dom-xss.md) — Ch. 6 — Batch 2
- [Event-Handler XSS](book1/xss/event-handler-xss.md) — Ch. 6 — Batch 2
- [HTML Context Breakout for XSS](book1/xss/html-context-breakout.md) — Ch. 6 — Batch 2
- [JavaScript and Data-URL XSS](book1/xss/javascript-data-url-xss.md) — Ch. 6 — Batch 2
- [Reflected XSS](book1/xss/reflected-xss.md) — Ch. 6 — Batch 2
- [Self-XSS](book1/xss/self-xss.md) — Ch. 6 — Batch 2
- [Stored XSS](book1/xss/stored-xss.md) — Ch. 6 — Batch 2
- [XSS Bypass: Alternative Syntax](book1/xss/bypass-alternative-syntax.md) — Ch. 6 — Batch 2
- [XSS Bypass: Capitalization and Encoding](book1/xss/bypass-case-and-encoding.md) — Ch. 6 — Batch 2
- [XSS Bypass: Filter Recomposition](book1/xss/bypass-filter-recomposition.md) — Ch. 6 — Batch 2
- [XSS Impact: Cookie Exfiltration](book1/xss/cookie-exfiltration-impact.md) — Ch. 6 — Batch 2
- [XSS Impact: CSRF Token Extraction](book1/xss/csrf-token-exfiltration.md) — Ch. 6 — Batch 2
- [XSS Input-Point Discovery](book1/xss/xss-input-point-discovery.md) — Ch. 6 — Batch 2
- [XSS Polyglot and Special-Character Probing](book1/xss/polyglot-special-char-probing.md) — Ch. 6 — Batch 2

### By Chapter

#### Chapter 4

- [Burp Browser + Proxy Setup](book1/misc/burp-proxy-browser-setup.md)
- [Burp Comparer Response Diffing](book1/misc/burp-comparer-response-diffing.md)
- [Burp Decoder for Encoded Application Data](book1/misc/burp-decoder-encoded-data.md)
- [Burp HTTPS Interception](book1/misc/burp-https-interception.md)
- [Burp Intruder Request Fuzzing](book1/misc/burp-intruder-request-fuzzing.md)
- [Burp Proxy Request Tampering](book1/misc/burp-proxy-request-tampering.md)
- [Burp Repeater Manual Request Testing](book1/misc/burp-repeater-manual-testing.md)
- [Save Burp Requests as Reproducible Artifacts](book1/misc/save-burp-request-as-curl.md)

#### Chapter 5

- [Bash Recon Wrapper](book1/recon/bash-recon-wrapper.md)
- [Building a Master Recon Report](book1/recon/master-recon-report.md)
- [Certificate SAN Host Enumeration](book1/recon/certificate-san-enumeration.md)
- [crt.sh JSON Automation](book1/recon/crtsh-json-automation.md)
- [Diff-Based Attack-Surface Monitoring](book1/recon/diff-based-attack-surface-monitoring.md)
- [Directory and File Brute-Forcing](book1/recon/directory-bruteforce.md)
- [GitHub Secret and Source Recon](book1/recon/github-secret-recon.md)
- [Google Dorking for Target Recon](book1/recon/google-dorking.md)
- [Interactive Recon Loop](book1/recon/interactive-recon-loop.md)
- [IP Range and ASN Discovery](book1/recon/ip-range-asn-discovery.md)
- [Manual Attack-Surface Walkthrough](book1/recon/manual-attack-surface-walk.md)
- [Multi-Domain Recon with getopts](book1/recon/multi-domain-getopts-recon.md)
- [OSINT for Technology and Internal Clues](book1/recon/osint-tech-stack-leaks.md)
- [Parsing Nmap Output with grep](book1/recon/grep-nmap-results.md)
- [Reusable Recon Function Library](book1/recon/reusable-recon-functions.md)
- [S3 Bucket Discovery and Access Testing](book1/recon/s3-bucket-recon.md)
- [Saving Recon Output with Redirection](book1/recon/recon-output-redirection.md)
- [Scheduled Continuous Recon with cron](book1/recon/cron-continuous-recon.md)
- [Selective Recon Scan Modes](book1/recon/recon-scan-modes.md)
- [Service Enumeration](book1/recon/service-enumeration.md)
- [Subdomain Enumeration](book1/recon/subdomain-enumeration.md)
- [Technology Stack Fingerprinting](book1/recon/tech-stack-fingerprinting.md)
- [Wayback Endpoint Discovery](book1/recon/wayback-endpoint-discovery.md)
- [Web Spidering / Crawling](book1/recon/web-spidering.md)
- [WHOIS and Reverse-WHOIS Scope Discovery](book1/recon/whois-reverse-whois.md)

#### Chapter 6

- [Blind XSS](book1/xss/blind-xss.md)
- [DOM-Based XSS](book1/xss/dom-xss.md)
- [Event-Handler XSS](book1/xss/event-handler-xss.md)
- [HTML Context Breakout for XSS](book1/xss/html-context-breakout.md)
- [JavaScript and Data-URL XSS](book1/xss/javascript-data-url-xss.md)
- [Reflected XSS](book1/xss/reflected-xss.md)
- [Self-XSS](book1/xss/self-xss.md)
- [Stored XSS](book1/xss/stored-xss.md)
- [XSS Bypass: Alternative Syntax](book1/xss/bypass-alternative-syntax.md)
- [XSS Bypass: Capitalization and Encoding](book1/xss/bypass-case-and-encoding.md)
- [XSS Bypass: Filter Recomposition](book1/xss/bypass-filter-recomposition.md)
- [XSS Impact: Cookie Exfiltration](book1/xss/cookie-exfiltration-impact.md)
- [XSS Impact: CSRF Token Extraction](book1/xss/csrf-token-exfiltration.md)
- [XSS Input-Point Discovery](book1/xss/xss-input-point-discovery.md)
- [XSS Polyglot and Special-Character Probing](book1/xss/polyglot-special-char-probing.md)

#### Chapter 7

- [Open Redirect Browser Autocorrect Bypass](book1/open-redirect-browser-autocorrect-bypass.md)
- [Open Redirect Bypass Chaining](book1/open-redirect-bypass-chaining.md)
- [Open Redirect Data URL Bypass](book1/open-redirect-data-url-bypass.md)
- [Open Redirect Double-Encoding Bypass](book1/open-redirect-double-encoding-bypass.md)
- [Open Redirect Google Dorks](book1/open-redirect-google-dorks.md)
- [Open Redirect Parameter Discovery](book1/open-redirect-parameter-discovery.md)
- [Open Redirect Security Impact Chaining](book1/open-redirect-security-impact.md)
- [Open Redirect Unicode Normalization Bypass](book1/open-redirect-unicode-normalization-bypass.md)
- [Open Redirect Validator Logic Bypass](book1/open-redirect-validator-logic-bypass.md)
- [Parameter-Based Open Redirect Test](book1/open-redirect-parameter-test.md)
- [Referer-Based Open Redirect](book1/referer-based-open-redirect.md)

#### Chapter 8

- [Clickjacking Double-Iframe Frame-Busting Bypass](book1/clickjacking-double-iframe-bypass.md)
- [Clickjacking Frameability Test](book1/clickjacking-frameability-test.md)
- [Clickjacking Impact Chaining](book1/clickjacking-impact-chaining.md)
- [Clickjacking Overlay PoC](book1/clickjacking-overlay-poc.md)
- [Clickjacking Protection Audit](book1/clickjacking-protection-audit.md)

#### Chapter 9

- [CSRF + Self-XSS to Stored XSS](book1/csrf-self-xss-chain.md)
- [CSRF Account-Takeover Chain](book1/csrf-account-takeover-chain.md)
- [CSRF Auto-Submitting HTML Form PoC](book1/csrf-html-form-poc.md)
- [CSRF Cross-Session Token Bypass](book1/csrf-cross-session-token-bypass.md)
- [CSRF Double-Submit Cookie Bypass](book1/csrf-double-submit-cookie-bypass.md)
- [CSRF Missing or Blank Token Bypass](book1/csrf-missing-blank-token-bypass.md)
- [CSRF Protection Bypass via XSS](book1/csrf-xss-chain.md)
- [CSRF Referer-Header Bypass](book1/csrf-referer-header-bypass.md)
- [CSRF Request-Method Switch Bypass](book1/csrf-method-switch-bypass.md)
- [CSRF State-Changing Request Discovery](book1/csrf-state-changing-request-discovery.md)
- [CSRF to Information Disclosure Chain](book1/csrf-info-leak-chain.md)
- [CSRF via Clickjacking Chain](book1/csrf-clickjacking-chain.md)

#### Chapter 10

- [Blind IDOR](book1/idor/blind-idor.md)
- [Encoded ID Bypass](book1/idor/encoded-id-bypass.md)
- [File Reference IDOR](book1/idor/file-reference-idor.md)
- [Hidden ID Parameter Injection](book1/idor/hidden-id-parameter-injection.md)
- [IDOR Authorization Automation with Burp](book1/idor/authorization-automation-burp.md)
- [IDOR File Extension Bypass](book1/idor/file-extension-bypass.md)
- [IDOR HTTP Method Switch Bypass](book1/idor/http-method-switch-bypass.md)
- [Leaked ID Chaining](book1/idor/leaked-id-chaining.md)
- [Numeric ID Swap IDOR](book1/idor/numeric-id-swap.md)
- [Predictable Randomized ID Analysis](book1/idor/predictable-randomized-id-analysis.md)
- [Two-Account Authorization Testing](book1/idor/two-account-authorization-testing.md)

#### Chapter 11

- [Boolean-Based Blind SQL Injection](book1/injection/blind-sql-boolean.md)
- [Error-Based SQL Injection](book1/injection/sql-error-based.md)
- [MongoDB `$ne` Authentication Bypass](book1/injection/nosql-mongodb-ne-auth-bypass.md)
- [NoSQL Injection Probing](book1/injection/nosql-injection-probing.md)
- [Second-Order SQL Injection](book1/injection/second-order-sql-injection.md)
- [SQL Database Fingerprinting](book1/injection/sql-database-fingerprinting.md)
- [SQL Injection Authentication Bypass with Comments](book1/injection/sql-auth-bypass-comment.md)
- [SQL Injection Automation with sqlmap](book1/injection/sqlmap-automation.md)
- [SQL Injection OUTFILE Exfiltration](book1/injection/sql-outfile-exfiltration.md)
- [SQL Injection Single-Quote Probe](book1/injection/sql-single-quote-probe.md)
- [SQL Injection to Web Shell via OUTFILE](book1/injection/sql-web-shell-outfile.md)
- [SQL Schema Enumeration](book1/injection/sql-schema-enumeration.md)
- [Time-Based Blind SQL Injection](book1/injection/blind-sql-time.md)
- [UNION-Based SQL Injection](book1/injection/sql-union-based.md)

#### Chapter 12

- [Race Condition Remediation with Resource Locking](book1/race-conditions/resource-locking-remediation.md)
- [Race Condition Result Validation](book1/race-conditions/race-condition-result-validation.md)
- [Race Condition Target Selection](book1/race-conditions/race-condition-target-selection.md)
- [Simultaneous Requests with `curl`](book1/race-conditions/simultaneous-curl-requests.md)
- [TOCTOU Race Condition](book1/race-conditions/toctou-race-condition.md)

#### Chapter 13

- [Blind SSRF OOB Detection](book1/blind-ssrf-oob-detection.md)
- [Blind SSRF Port Scanning](book1/blind-ssrf-port-scanning.md)
- [SSRF Allowlist Bypass via Open Redirect](book1/ssrf-allowlist-open-redirect-bypass.md)
- [SSRF AWS Instance Metadata Access](book1/ssrf-aws-instance-metadata.md)
- [SSRF Blocklist Bypass via Redirect](book1/ssrf-blocklist-redirect-bypass.md)
- [SSRF DNS Resolution Bypass](book1/ssrf-dns-resolution-bypass.md)
- [SSRF Entry-Point Discovery](book1/ssrf-entry-point-discovery.md)
- [SSRF Google Cloud Metadata Access](book1/ssrf-google-cloud-metadata.md)
- [SSRF Internal API Access](book1/ssrf-internal-api-access.md)
- [SSRF Internal Network Scanning](book1/ssrf-internal-network-scanning.md)
- [SSRF Internal Port Scanning](book1/ssrf-internal-port-scanning.md)
- [SSRF Internal URL Probing](book1/ssrf-internal-url-probing.md)
- [SSRF IP Encoding Bypass](book1/ssrf-ip-encoding-bypass.md)
- [SSRF IPv6 Blocklist Bypass](book1/ssrf-ipv6-bypass.md)
- [SSRF Regex Allowlist Bypass](book1/ssrf-allowlist-regex-bypass.md)

#### Chapter 14

- [Insecure Deserialization Hunting](book1/deserialization-hunting.md)
- [Java Deserialization Gadget Chains](book1/java-deserialization-gadget-chain.md)
- [Java Serialized Object Recognition](book1/java-serialized-object-recognition.md)
- [Java Serialized Object Tampering](book1/java-serialized-object-tampering.md)
- [PHP Magic-Method Deserialization RCE](book1/php-magic-method-rce.md)
- [PHP POP-Chain Deserialization](book1/php-pop-chain-rce.md)
- [PHP Serialized Object Recognition](book1/php-serialized-object-recognition.md)
- [PHP Serialized Property Tampering](book1/php-object-property-tampering.md)
- [Ysoserial Java Deserialization Payloads](book1/ysoserial-java-deserialization.md)

#### Chapter 15

- [Blind XXE Error-Based Exfiltration](book1/blind-xxe-error-exfiltration.md)
- [Blind XXE External-DTD Exfiltration](book1/blind-xxe-external-dtd-exfiltration.md)
- [Blind XXE OOB Detection](book1/blind-xxe-oob-detection.md)
- [Classic XXE File Read](book1/classic-xxe-file-read.md)
- [XInclude File Read](book1/xinclude-file-read.md)
- [XXE Billion-Laughs / XML Bomb](book1/xxe-billion-laughs-dos.md)
- [XXE CDATA Exfiltration](book1/xxe-cdata-exfiltration.md)
- [XXE Entry-Point Discovery](book1/xxe-entry-point-discovery.md)
- [XXE FTP Exfiltration](book1/xxe-ftp-exfiltration.md)
- [XXE in Office Document Archives](book1/xxe-office-document-smuggling.md)
- [XXE PHP-Filter Base64 Exfiltration](book1/xxe-php-filter-base64-exfiltration.md)
- [XXE via SVG Upload](book1/xxe-svg-upload.md)
- [XXE-to-SSRF](book1/xxe-ssrf.md)

#### Chapter 16

- [Jinja2 `catch_warnings` Sandbox Escape](book1/jinja2-catch-warnings-sandbox-escape.md)
- [Jinja2 Command-Execution PoC](book1/jinja2-command-execution-poc.md)
- [Jinja2 Sandbox Class Enumeration](book1/jinja2-sandbox-class-enumeration.md)
- [SSTI Arithmetic Probes](book1/ssti-arithmetic-probes.md)
- [SSTI Automation with Tplmap](book1/ssti-tplmap-automation.md)
- [SSTI Error-Probe Detection](book1/ssti-error-probe.md)
- [SSTI Input-Point Discovery](book1/ssti-input-discovery.md)
- [SSTI Template-Engine Fingerprinting](book1/ssti-engine-fingerprinting.md)

#### Chapter 17

- [Cookie-Based Access-Control Bypass](book1/cookie-based-access-control-bypass.md)
- [Directory Traversal via Filepath Input](book1/directory-traversal-basic.md)
- [Exposed Admin Panel Discovery](book1/exposed-admin-panel-discovery.md)
- [Forced Browsing Access-Control Bypass](book1/forced-browsing-access-control-bypass.md)
- [Payment Verification Parameter Bypass](book1/payment-verification-parameter-bypass.md)
- [Skippable Authentication Step](book1/skippable-authentication-step.md)

#### Chapter 18

- [Blind RCE Out-of-Band Confirmation](book1/rce-oob-callback.md)
- [Blind RCE via Time Delay](book1/blind-rce-time-delay.md)
- [Classic RCE Verification](book1/classic-rce-verification.md)
- [Duplicate-Parameter RCE Filter Bypass](book1/http-parameter-splitting-rce-bypass.md)
- [Local File Inclusion (LFI) via Uploaded File](book1/local-file-inclusion.md)
- [PHP Code-Execution Filter Bypass](book1/php-rce-filter-bypass.md)
- [Python Code-Execution Filter Bypass](book1/python-rce-filter-bypass.md)
- [Python eval() Code Injection](book1/python-eval-code-injection.md)
- [Remote File Inclusion (RFI)](book1/remote-file-inclusion.md)
- [Safe RCE Proof of Concept](book1/rce-safe-proof-of-concept.md)
- [Shell Command Injection](book1/shell-command-injection.md)
- [Unix Command Filter Bypass](book1/unix-command-filter-bypass.md)

#### Chapter 19

- [CORS Arbitrary Origin Reflection](book1/cors-arbitrary-origin-reflection.md)
- [CORS null-Origin Misconfiguration](book1/cors-null-origin.md)
- [CORS Weak Regex Origin Bypass](book1/cors-regex-origin-bypass.md)
- [JSONP Sensitive Data Exposure](book1/jsonp-sensitive-data-exposure.md)
- [postMessage Missing Sender-Origin Validation](book1/postmessage-missing-sender-validation.md)
- [postMessage Wildcard Target-Origin Leak](book1/postmessage-wildcard-target-origin.md)
- [SOP Relaxation Fingerprinting](book1/sop-relaxation-fingerprinting.md)

#### Chapter 20

- [Continuous Subdomain Takeover Monitoring](book1/subdomain-takeover-monitoring.md)
- [Dangling CNAME Subdomain Takeover](book1/subdomain-takeover-dangling-cname.md)
- [OAuth Token Lifetime / Revocation Test](book1/oauth-token-lifetime-test.md)
- [OAuth Token Theft via Open Redirect](book1/oauth-open-redirect-token-theft.md)
- [OAuth Token Theft via Redirect Chain](book1/oauth-open-redirect-chain.md)
- [SAML Empty/Removed Signature Bypass](book1/saml-empty-signature-bypass.md)
- [SAML Predictable Signature Forgery](book1/saml-predictable-signature-forgery.md)
- [SAML Response Editing and Re-encoding](book1/saml-raider-edit-reencode.md)
- [SAML Unsigned Assertion Tampering](book1/saml-unsigned-assertion-tampering.md)
- [Shared-Cookie + Subdomain Takeover Chain](book1/shared-cookie-subdomain-takeover-chain.md)
- [SSO Mechanism Fingerprinting](book1/sso-mechanism-fingerprinting.md)

#### Chapter 21

- [Decompress Exposed Git Objects](book1/git-object-decompression.md)
- [Exposed .git Directory Detection](book1/exposed-git-directory-detection.md)
- [Manual .git Reconstruction](book1/exposed-git-manual-reconstruction.md)
- [Paste Dump Secret Search](book1/paste-dump-secret-search.md)
- [Path Traversal Encoding Bypass](book1/path-traversal-encoding-bypass.md)
- [Public JavaScript Secret Hunting](book1/public-js-secret-hunting.md)
- [Recursive Download of Exposed .git](book1/exposed-git-recursive-download.md)
- [Software Version Disclosure](book1/software-version-disclosure.md)
- [Wayback Sensitive File Discovery](book1/wayback-sensitive-file-discovery.md)

#### Chapter 22

- [Code Review: Developer Comments and Debug Endpoints](book1/code-review-comments-debug-endpoints.md)
- [Code Review: Grep for Dangerous Sinks](book1/code-review-dangerous-sinks-grep.md)
- [Code Review: Hardcoded Secret Hunting](book1/code-review-secret-grep.md)
- [Code Review: Incomplete CSRF Validation](book1/code-review-csrf-bypass-review.md)
- [Code Review: One Input, Multiple Vulnerable Sinks](book1/code-review-multi-sink-input-tracing.md)
- [Code Review: Outdated Dependency Review](book1/code-review-dependency-cve-review.md)
- [Code Review: Trace Security-Critical Functions](book1/code-review-sensitive-flow-tracing.md)
- [Code Review: User-Input Taint Tracing](book1/code-review-user-input-taint-tracing.md)
- [Code Review: Weak Cryptography Search](book1/code-review-weak-crypto-grep.md)
- [Code Review: Weak Redirect Validation](book1/code-review-open-redirect-validation-review.md)
- [SAST-Assisted Source Code Review](book1/sast-assisted-code-review.md)

#### Chapter 23

- [Android: ADB Device and File Workflow](book1/android-adb-basics.md)
- [Android: APK and AndroidManifest Recon](book1/android-apk-manifest-recon.md)
- [Android: Apktool Decompile and Rebuild](book1/android-apktool-decompile-rebuild.md)
- [Android: Bypass Certificate Pinning with Frida/Objection](book1/android-cert-pinning-objection-frida.md)
- [Android: Compare Mobile vs Web Authorization](book1/android-mobile-web-auth-diff-testing.md)
- [Android: Frida Runtime Instrumentation](book1/android-frida-runtime-analysis.md)
- [Android: Hunt Hardcoded Secrets in APK Resources](book1/android-hardcoded-secret-hunting.md)
- [Android: Install Burp CA for HTTPS Interception](book1/android-burp-ca-install.md)
- [Android: MobSF Static and Dynamic Triage](book1/android-mobsf-static-dynamic-analysis.md)
- [Android: Review Bundled SQLite/DB Files](book1/android-sqlite-sensitive-data-review.md)
- [Android: Route App Traffic Through Burp](book1/android-burp-proxy-setup.md)

#### Chapter 24

- [API Recon: Capture Workflows and Deduce Hidden Endpoints](book1/api-workflow-capture-endpoint-deduction.md)
- [API Recon: Public and Exposed Swagger Documentation](book1/api-documentation-swagger-recon.md)
- [API Recon: Test Older API Versions](book1/api-version-downgrade-testing.md)
- [API: Access-Token Lifecycle Testing](book1/api-token-lifecycle-testing.md)
- [API: BOLA/IDOR Testing](book1/api-bola-idor-testing.md)
- [API: Excessive Data Exposure](book1/api-excessive-data-exposure.md)
- [API: HTTP Method Authorization Bypass](book1/api-method-access-control-bypass.md)
- [API: Rate-Limit Testing](book1/api-rate-limit-testing.md)
- [API: Re-test Web Injection Classes Through API Inputs](book1/api-technical-injection-surface.md)
- [GraphQL: Endpoint Discovery](book1/graphql-endpoint-discovery.md)
- [GraphQL: Enumerate Fields with __type](book1/graphql-type-field-enum.md)
- [GraphQL: Enumerate Types with Introspection](book1/graphql-introspection-schema-enum.md)
- [GraphQL: Mutation Authorization Testing](book1/graphql-mutation-authorization-testing.md)
- [GraphQL: Recon When Introspection Is Disabled](book1/graphql-introspection-disabled-recon.md)
- [SOAP: WSDL Endpoint Discovery](book1/soap-wsdl-discovery.md)

#### Chapter 25

- [Burp Intruder: Fuzzing Workflow](book1/burp-intruder-fuzzing-workflow.md)
- [Fuzzing: Map Data Injection Points](book1/fuzzing-injection-point-mapping.md)
- [Fuzzing: Payload List Strategy](book1/fuzzing-payload-list-strategy.md)
- [Fuzzing: Triage Response Anomalies](book1/fuzzing-response-anomaly-triage.md)
- [Wfuzz: Basic Authentication Fuzzing](book1/wfuzz-basic-auth-bruteforce.md)
- [Wfuzz: IDOR/BOLA Enumeration](book1/wfuzz-idor-fuzzing.md)
- [Wfuzz: Open Redirect Fuzzing](book1/wfuzz-open-redirect-fuzzing.md)
- [Wfuzz: Path Enumeration](book1/wfuzz-path-enumeration.md)
- [Wfuzz: Reflected XSS Fuzzing](book1/wfuzz-reflected-xss-fuzzing.md)
- [Wfuzz: SQL Injection Fuzzing](book1/wfuzz-sqli-fuzzing.md)

## Book 2 — Real-World Bug Hunting — A Field Guide to Web Hacking

**Author:** Peter Yaworski

### By Category

#### API Security

- [CSRF Testing on API Endpoints](book2/api-security/csrf-api-endpoint-testing.md) — Ch. 4 — Batch 1

#### Miscellaneous

- [HTTP OPTIONS Method Enumeration](book2/misc/http-options-method-enumeration.md) — Ch. 1 — Batch 1
- [Open Redirect Parameter Hunting](book2/misc/open-redirect-parameter-hunting.md) — Ch. 2 — Batch 1
- [Open Redirect Through a Trusted Third-Party Chain](book2/misc/open-redirect-third-party-chain.md) — Ch. 2 — Batch 1
- [Open Redirect via Meta Refresh or JavaScript](book2/misc/open-redirect-meta-js-sinks.md) — Ch. 2 — Batch 1
- [Partial-URL Open Redirect Bypass](book2/misc/open-redirect-partial-url-special-character-bypass.md) — Ch. 2 — Batch 1
- [Client-Side HPP with Encoded Ampersand](book2/misc/hpp-client-side-encoded-ampersand.md) — Ch. 3 — Batch 1
- [HPP in Third-Party Service Handoffs](book2/misc/hpp-third-party-handoff.md) — Ch. 3 — Batch 1
- [HPP Signature-Validation / Action Split](book2/misc/hpp-signature-validation-action-split.md) — Ch. 3 — Batch 1
- [HPP UI / Action Parameter Desynchronization](book2/misc/hpp-ui-action-parameter-desync.md) — Ch. 3 — Batch 1
- [HTTP Parameter Pollution: Duplicate Parameter Precedence](book2/misc/hpp-duplicate-parameter-precedence.md) — Ch. 3 — Batch 1
- [HTTP Parameter Pollution: Hidden Parameter Injection](book2/misc/hpp-hidden-parameter-injection.md) — Ch. 3 — Batch 1
- [CSRF Content-Type / Preflight Bypass](book2/misc/csrf-content-type-preflight-bypass.md) — Ch. 4 — Batch 1
- [CSRF Origin, Referer, and SameSite Review](book2/misc/csrf-origin-referer-samesite-review.md) — Ch. 4 — Batch 1
- [CSRF Through a State-Changing GET](book2/misc/csrf-state-changing-get-img.md) — Ch. 4 — Batch 1
- [CSRF Token Leak Through Cross-Origin JavaScript](book2/misc/csrf-token-leak-cross-origin-script.md) — Ch. 4 — Batch 1
- [CSRF Token Removal and Tampering Test](book2/misc/csrf-token-removal-tampering.md) — Ch. 4 — Batch 1
- [CSRF with an Auto-Submitted POST Form](book2/misc/csrf-post-hidden-form-autosubmit.md) — Ch. 4 — Batch 1
- [HTML Entity Decoding Filter Bypass](book2/html-entity-decoding-bypass.md) — Ch. 5 — Batch 2
- [HTML Injection: Fake Form Injection](book2/html-injection-phishing-form.md) — Ch. 5 — Batch 2
- [Markdown Hanging-Quote + Meta Refresh Exfiltration](book2/markdown-hanging-quote-meta-refresh.md) — Ch. 5 — Batch 2
- [Markdown Parser Attribute Confusion](book2/markdown-parser-attribute-confusion.md) — Ch. 5 — Batch 2
- [React `dangerouslySetInnerHTML` Sink Review](book2/react-dangerouslysetinnerhtml-sink.md) — Ch. 5 — Batch 2
- [URI-Decoding Render Test](book2/uri-decoding-render-test.md) — Ch. 5 — Batch 2
- [URL Parameter Content Spoofing](book2/url-parameter-content-spoofing.md) — Ch. 5 — Batch 2
- [CRLF `Location` Header Injection Chain](book2/crlf-location-header-chain.md) — Ch. 6 — Batch 2
- [CRLF Header Injection Probe](book2/crlf-header-injection-probe.md) — Ch. 6 — Batch 2
- [CRLF HTTP Response Splitting](book2/crlf-response-splitting.md) — Ch. 6 — Batch 2
- [CRLF Multibyte Unicode Blacklist Bypass](book2/crlf-multibyte-unicode-bypass.md) — Ch. 6 — Batch 2
- [CRLF-to-XSS Response Chain](book2/crlf-to-xss-chain.md) — Ch. 6 — Batch 2
- [`javascript:` URL in an `href` Sink](book2/javascript-url-href-xss.md) — Ch. 7 — Batch 2
- [Basic Script-Tag XSS Probe](book2/script-tag-basic-probe.md) — Ch. 7 — Batch 2
- [Blind XSS in Privileged Render Paths](book2/blind-xss-admin-render.md) — Ch. 7 — Batch 2
- [DOM XSS via `location.hash` to `innerHTML`](book2/dom-xss-location-hash-innerhtml.md) — Ch. 7 — Batch 2
- [Iframe `javascript:` Scheme Context Bypass](book2/iframe-javascript-scheme-context-bypass.md) — Ch. 7 — Batch 2
- [JavaScript Function-Override Filter Bypass](book2/javascript-function-override-bypass.md) — Ch. 7 — Batch 2
- [JavaScript String-Context Breakout](book2/javascript-string-breakout.md) — Ch. 7 — Batch 2
- [Malformed Boolean-Attribute Sanitizer Bypass](book2/malformed-boolean-attribute-sanitizer-bypass.md) — Ch. 7 — Batch 2
- [Self-XSS Chaining with Login/Logout CSRF](book2/self-xss-chain-login-csrf.md) — Ch. 7 — Batch 2
- [Stored XSS Across Secondary Render Locations](book2/stored-xss-multi-render-location.md) — Ch. 7 — Batch 2
- [XSS Attribute Breakout with `autofocus` + `onfocus`](book2/html-attribute-breakout-autofocus.md) — Ch. 7 — Batch 2
- [XSS Filter Bypass with `document.writeln` + URL Fragment](book2/document-writeln-location-hash-bypass.md) — Ch. 7 — Batch 2
- [XSS via Alternate Input Path](book2/alternate-input-path-sanitization-bypass.md) — Ch. 7 — Batch 2
- [AngularJS CSTI Probe and Version Check](book2/angularjs-csti-probe-and-version.md) — Ch. 8 — Batch 2
- [AngularJS Sandbox Escape Testing](book2/angularjs-sandbox-escape.md) — Ch. 8 — Batch 2
- [Cross-Service SSTI via Email Rendering](book2/cross-service-ssti-email-render.md) — Ch. 8 — Batch 2
- [Jinja2 Introspection as SSTI Impact Proof](book2/jinja2-introspection-proof.md) — Ch. 8 — Batch 2
- [Rails Dynamic `render` Path Traversal](book2/rails-dynamic-render-path-traversal.md) — Ch. 8 — Batch 2
- [Rails ERB Dynamic Render Code Execution Probe](book2/rails-erb-render-rce-probe.md) — Ch. 8 — Batch 2
- [Smarty `{php}` Tag Code-Execution Proof](book2/smarty-php-tag-code-execution.md) — Ch. 8 — Batch 2
- [Smarty SSTI Error + Version Probe](book2/smarty-error-and-version-probe.md) — Ch. 8 — Batch 2
- [Smarty/PHP File-Read Chunking](book2/smarty-file-read-chunking.md) — Ch. 8 — Batch 2
- [SSTI Arithmetic Fingerprinting](book2/ssti-arithmetic-fingerprinting.md) — Ch. 8 — Batch 2
- [Blind SQLi Character-by-Character Extraction](book2/blind-sqli-character-bruteforce.md) — Ch. 9 — Batch 3
- [Blind SQLi Database-Version Boolean Test](book2/blind-sqli-version-boolean.md) — Ch. 9 — Batch 3
- [Blind SQLi Python Automation Pattern](book2/blind-sqli-python-automation-pattern.md) — Ch. 9 — Batch 3
- [Blind SQLi via Result Differential](book2/blind-sqli-result-differential.md) — Ch. 9 — Batch 3
- [Drupal `IN` Placeholder SQLi Pattern](book2/drupal-in-placeholder-sqli.md) — Ch. 9 — Batch 3
- [SQLi Comment-Out Query Tail](book2/sqli-comment-tail-bypass.md) — Ch. 9 — Batch 3
- [SQLi Inside Base64-Encoded JSON](book2/sqli-base64-json-parameter.md) — Ch. 9 — Batch 3
- [SQLi Quote + Boolean Probe](book2/sqli-quote-and-boolean-probe.md) — Ch. 9 — Batch 3
- [SQLi via Array Parameter Structure Change](book2/sqli-array-parameter-structure-change.md) — Ch. 9 — Batch 3
- [Time-Based Blind SQLi with `sleep()`](book2/time-based-blind-sqli-sleep.md) — Ch. 9 — Batch 3
- [Blind SSRF OOB DNS Exfiltration](book2/ssrf-oob-dns-exfiltration.md) — Ch. 10 — Batch 3
- [Blind SSRF Timing-Based Port Scan](book2/blind-ssrf-timing-port-scan.md) — Ch. 10 — Batch 3
- [SSRF AWS Metadata Hostname Probe](book2/aws-metadata-hostname-probe.md) — Ch. 10 — Batch 3
- [SSRF Extension Filter Bypass with Query Delimiter](book2/ssrf-extension-filter-bypass-query.md) — Ch. 10 — Batch 3
- [SSRF External-to-Internal Redirect Bypass](book2/external-to-internal-redirect-bypass.md) — Ch. 10 — Batch 3
- [SSRF GET vs POST Capability Check](book2/ssrf-get-vs-post-capability.md) — Ch. 10 — Batch 3
- [SSRF into Internal DNS](book2/internal-dns-ssrf.md) — Ch. 10 — Batch 3
- [SSRF Localhost Filter Bypass with Alternate IP Notation](book2/webhook-localhost-alternate-notation.md) — Ch. 10 — Batch 3
- [SSRF Response-to-XSS Chain](book2/ssrf-response-to-xss.md) — Ch. 10 — Batch 3
- [SSRF URL-Parameter Discovery](book2/ssrf-url-parameter-discovery.md) — Ch. 10 — Batch 3
- [Blind XXE External Callback](book2/xxe-oob-external-callback.md) — Ch. 11 — Batch 3
- [Python SimpleHTTPServer as XXE Callback Listener](book2/python-simplehttpserver-oob-listener.md) — Ch. 11 — Batch 3
- [XXE by Preserving Native XML Structure](book2/xxe-preserve-native-xml-structure.md) — Ch. 11 — Batch 3
- [XXE External DTD File Exfiltration](book2/xxe-external-dtd-file-exfil.md) — Ch. 11 — Batch 3
- [XXE in Office Document Uploads](book2/xxe-office-docx-upload.md) — Ch. 11 — Batch 3
- [XXE Local File Read](book2/xxe-local-file-read.md) — Ch. 11 — Batch 3
- [Arbitrary File Write to SSH `authorized_keys`](book2/arbitrary-file-write-ssh-authorized-keys.md) — Ch. 12 — Batch 3
- [Command Flag Injection After Shell Escaping](book2/command-flag-injection-after-escaping.md) — Ch. 12 — Batch 3
- [ImageMagick Delegate Command Injection](book2/imagemagick-delegate-command-injection.md) — Ch. 12 — Batch 3
- [ImageMagick Extension-Only Upload Bypass](book2/imagemagick-content-type-extension-bypass.md) — Ch. 12 — Batch 3
- [Netcat Callback Listener for RCE Proof](book2/netcat-http-callback-listener.md) — Ch. 12 — Batch 3
- [OS Command Injection via Semicolon](book2/os-command-injection-semicolon.md) — Ch. 12 — Batch 3
- [Path Traversal to Arbitrary File Write](book2/path-traversal-arbitrary-file-write.md) — Ch. 12 — Batch 3
- [PHP `call_user_func` Function Injection](book2/php-call-user-func-function-injection.md) — Ch. 12 — Batch 3
- [Public Repository Secret Recon with Gitrob](book2/gitrob-secret-key-recon.md) — Ch. 12 — Batch 3
- [Rails `secret_key_base` Cookie-Forgery Risk](book2/rails-secret-key-cookie-forgery-risk.md) — Ch. 12 — Batch 3
- [Rails Signed-Cookie Deserialization RCE](book2/rails-signed-cookie-deserialization-rce.md) — Ch. 12 — Batch 3
- [Subdomain + Port + Screenshot Recon Workflow](book2/subdomain-port-screenshot-workflow.md) — Ch. 12 — Batch 3
- [Unrestricted PHP Upload to Code Execution](book2/unrestricted-php-upload-rce.md) — Ch. 12 — Batch 3
- [`memcpy()` Source/Destination Size Audit](book2/memcpy-source-destination-size-audit.md) — Ch. 13 — Batch 4
- [Buffer Overflow Length-Check Review](book2/buffer-overflow-length-check-review.md) — Ch. 13 — Batch 4
- [libcurl POST Buffer Read-Out-of-Bounds Pattern](book2/libcurl-post-buffer-read-oob.md) — Ch. 13 — Batch 4
- [Managed-Language Native Extension Overflow Hunting](book2/native-extension-overflow-hunting.md) — Ch. 13 — Batch 4
- [Read-Out-of-Bounds Length Mismatch](book2/read-out-of-bounds-heartbleed-pattern.md) — Ch. 13 — Batch 4
- [Certificate Transparency Subdomain Enumeration](book2/certificate-transparency-subdomain-enum.md) — Ch. 14 — Batch 4
- [CNAME to Unregistered Domain Takeover](book2/unregistered-domain-cname-takeover.md) — Ch. 14 — Batch 4
- [Dangling CNAME Subdomain Takeover](book2/subdomain-takeover-dangling-cname.md) — Ch. 14 — Batch 4
- [Provider Error-Signature Takeover Testing](book2/provider-error-signature-takeover.md) — Ch. 14 — Batch 4
- [SendGrid Inbound Parse Domain Takeover](book2/sendgrid-inbound-parse-domain-takeover.md) — Ch. 14 — Batch 4
- [Subdomain Takeover Enumeration with KnockPy](book2/subdomain-takeover-knockpy.md) — Ch. 14 — Batch 4
- [Wildcard Certificate Hash Pivot with Censys](book2/wildcard-cert-censys-pivot.md) — Ch. 14 — Batch 4
- [Wildcard Third-Party Subdomain Override](book2/wildcard-third-party-subdomain-override.md) — Ch. 14 — Batch 4
- [Background Job Condition-Swap Race](book2/background-job-condition-swap.md) — Ch. 15 — Batch 4
- [Concurrent Request Limit Bypass with Burp](book2/burp-concurrent-limit-bypass.md) — Ch. 15 — Batch 4
- [Email Change vs Verification Race](book2/email-change-verification-race.md) — Ch. 15 — Batch 4
- [Manual Two-Browser Race Test](book2/manual-two-browser-race.md) — Ch. 15 — Batch 4
- [Race Condition / TOCTOU Identification](book2/race-condition-toctou-identification.md) — Ch. 15 — Batch 4
- [Hidden POST-Body IDOR Discovery](book2/hidden-post-body-id-discovery.md) — Ch. 16 — Batch 4
- [IDOR in Hidden Iframe Requests](book2/iframe-hidden-endpoint-idor.md) — Ch. 16 — Batch 4
- [IDOR Privilege Escalation via Account/Administration ID](book2/idor-privilege-escalation-via-admin-id.md) — Ch. 16 — Batch 4
- [IDOR Secret Leak to Account Takeover](book2/idor-secret-leak-to-account-takeover.md) — Ch. 16 — Batch 4
- [Sequential Numeric IDOR Enumeration](book2/simple-sequential-id-enumeration.md) — Ch. 16 — Batch 4
- [UUID IDOR with Two Controlled Accounts](book2/two-account-uuid-swap.md) — Ch. 16 — Batch 4
- [UUID Leakage Hunting for IDOR](book2/uuid-leak-hunting.md) — Ch. 16 — Batch 4
- [OAuth `redirect_uri` Prefix Validation Bypass](book2/oauth-redirect-uri-prefix-bypass.md) — Ch. 17 — Batch 4
- [OAuth `state` CSRF Validation](book2/oauth-state-csrf-validation.md) — Ch. 17 — Batch 4
- [OAuth Custom Registration Default-Password Flaw](book2/oauth-custom-registration-default-password.md) — Ch. 17 — Batch 4
- [OAuth Forgotten Whitelisted Domain Takeover](book2/oauth-forgotten-whitelisted-domain-takeover.md) — Ch. 17 — Batch 4
- [OAuth-Like Redirect Bypass via URL Userinfo Parsing](book2/oauth-wreply-userinfo-parser-bypass.md) — Ch. 17 — Batch 4
- [2FA OTP Account-Binding Test](book2/two-factor-otp-account-binding-test.md) — Ch. 18 — Batch 4
- [CIDR Scan for Exposed `phpinfo.php`](book2/phpinfo-cidr-wget-scan.md) — Ch. 18 — Batch 4
- [EyeWitness Subdomain Visual Triage](book2/eyewitness-subdomain-triage.md) — Ch. 18 — Batch 4
- [Feature-Interaction Metric Manipulation](book2/feature-interaction-metric-manipulation.md) — Ch. 18 — Batch 4
- [Frontend-Only Permission Enforcement](book2/frontend-only-permission-check.md) — Ch. 18 — Batch 4
- [Hidden Endpoint Discovery in JavaScript](book2/javascript-hidden-endpoint-discovery.md) — Ch. 18 — Batch 4
- [Nmap Full-Port Version Scan](book2/nmap-full-port-version-scan.md) — Ch. 18 — Batch 4
- [Rails Mass Assignment](book2/rails-mass-assignment.md) — Ch. 18 — Batch 4
- [S3 Bucket Name Permutation Fuzzing](book2/s3-bucket-name-permutation-fuzzing.md) — Ch. 18 — Batch 4
- [S3 Public-Write Permission Test](book2/s3-public-write-test-aws-cli.md) — Ch. 18 — Batch 4
- [Unauthenticated Memcache Service Check](book2/memcache-unauthenticated-service-check.md) — Ch. 18 — Batch 4
- [Web vs Mobile Security-Control Bypass](book2/web-vs-mobile-security-check-bypass.md) — Ch. 18 — Batch 4
- [Burp Intruder Path Discovery](book2/burp-intruder-path-discovery.md) — Ch. 19 — Batch 5
- [Enumerating Subdomains of Subdomains](book2/subdomain-of-subdomain-enumeration.md) — Ch. 19 — Batch 5
- [Functionality-to-Vulnerability Mapping](book2/functionality-to-vulnerability-mapping.md) — Ch. 19 — Batch 5
- [Generic Injection Polyglot Probe](book2/generic-injection-polyglot-probe.md) — Ch. 19 — Batch 5
- [GitHub Repository Sensitive-Data Review](book2/github-repository-sensitive-data-review.md) — Ch. 19 — Batch 5
- [Gobuster File and Directory Discovery](book2/gobuster-content-discovery.md) — Ch. 19 — Batch 5
- [Google Dorking for Vulnerability-Relevant Parameters](book2/google-dork-vulnerable-parameters.md) — Ch. 19 — Batch 5
- [IP Outlier Prioritization](book2/ip-outlier-prioritization.md) — Ch. 19 — Batch 5
- [JavaScript File Change Monitoring](book2/javascript-file-change-monitoring.md) — Ch. 19 — Batch 5
- [Meg Multi-Host Path Discovery](book2/meg-multi-host-path-discovery.md) — Ch. 19 — Batch 5
- [Nmap + Masscan Port-Scanning Workflow](book2/nmap-masscan-port-workflow.md) — Ch. 19 — Batch 5
- [Retesting Previously Disclosed Bugs](book2/previous-bug-retest-methodology.md) — Ch. 19 — Batch 5
- [Screenshot-Based Visual Recon Triage](book2/screenshot-visual-triage.md) — Ch. 19 — Batch 5
- [SubFinder Subdomain Enumeration](book2/subfinder-subdomain-enumeration.md) — Ch. 19 — Batch 5
- [Technology-Stack-Driven Testing](book2/technology-stack-driven-testing.md) — Ch. 19 — Batch 5

#### Reconnaissance

- [DNS A-Record Lookup with dig](book2/recon/dns-a-record-dig.md) — Ch. 1 — Batch 1

### By Chapter

#### Chapter 1

- [DNS A-Record Lookup with dig](book2/recon/dns-a-record-dig.md)
- [HTTP OPTIONS Method Enumeration](book2/misc/http-options-method-enumeration.md)

#### Chapter 2

- [Open Redirect Parameter Hunting](book2/misc/open-redirect-parameter-hunting.md)
- [Open Redirect Through a Trusted Third-Party Chain](book2/misc/open-redirect-third-party-chain.md)
- [Open Redirect via Meta Refresh or JavaScript](book2/misc/open-redirect-meta-js-sinks.md)
- [Partial-URL Open Redirect Bypass](book2/misc/open-redirect-partial-url-special-character-bypass.md)

#### Chapter 3

- [Client-Side HPP with Encoded Ampersand](book2/misc/hpp-client-side-encoded-ampersand.md)
- [HPP in Third-Party Service Handoffs](book2/misc/hpp-third-party-handoff.md)
- [HPP Signature-Validation / Action Split](book2/misc/hpp-signature-validation-action-split.md)
- [HPP UI / Action Parameter Desynchronization](book2/misc/hpp-ui-action-parameter-desync.md)
- [HTTP Parameter Pollution: Duplicate Parameter Precedence](book2/misc/hpp-duplicate-parameter-precedence.md)
- [HTTP Parameter Pollution: Hidden Parameter Injection](book2/misc/hpp-hidden-parameter-injection.md)

#### Chapter 4

- [CSRF Content-Type / Preflight Bypass](book2/misc/csrf-content-type-preflight-bypass.md)
- [CSRF Origin, Referer, and SameSite Review](book2/misc/csrf-origin-referer-samesite-review.md)
- [CSRF Testing on API Endpoints](book2/api-security/csrf-api-endpoint-testing.md)
- [CSRF Through a State-Changing GET](book2/misc/csrf-state-changing-get-img.md)
- [CSRF Token Leak Through Cross-Origin JavaScript](book2/misc/csrf-token-leak-cross-origin-script.md)
- [CSRF Token Removal and Tampering Test](book2/misc/csrf-token-removal-tampering.md)
- [CSRF with an Auto-Submitted POST Form](book2/misc/csrf-post-hidden-form-autosubmit.md)

#### Chapter 5

- [HTML Entity Decoding Filter Bypass](book2/html-entity-decoding-bypass.md)
- [HTML Injection: Fake Form Injection](book2/html-injection-phishing-form.md)
- [Markdown Hanging-Quote + Meta Refresh Exfiltration](book2/markdown-hanging-quote-meta-refresh.md)
- [Markdown Parser Attribute Confusion](book2/markdown-parser-attribute-confusion.md)
- [React `dangerouslySetInnerHTML` Sink Review](book2/react-dangerouslysetinnerhtml-sink.md)
- [URI-Decoding Render Test](book2/uri-decoding-render-test.md)
- [URL Parameter Content Spoofing](book2/url-parameter-content-spoofing.md)

#### Chapter 6

- [CRLF `Location` Header Injection Chain](book2/crlf-location-header-chain.md)
- [CRLF Header Injection Probe](book2/crlf-header-injection-probe.md)
- [CRLF HTTP Response Splitting](book2/crlf-response-splitting.md)
- [CRLF Multibyte Unicode Blacklist Bypass](book2/crlf-multibyte-unicode-bypass.md)
- [CRLF-to-XSS Response Chain](book2/crlf-to-xss-chain.md)

#### Chapter 7

- [`javascript:` URL in an `href` Sink](book2/javascript-url-href-xss.md)
- [Basic Script-Tag XSS Probe](book2/script-tag-basic-probe.md)
- [Blind XSS in Privileged Render Paths](book2/blind-xss-admin-render.md)
- [DOM XSS via `location.hash` to `innerHTML`](book2/dom-xss-location-hash-innerhtml.md)
- [Iframe `javascript:` Scheme Context Bypass](book2/iframe-javascript-scheme-context-bypass.md)
- [JavaScript Function-Override Filter Bypass](book2/javascript-function-override-bypass.md)
- [JavaScript String-Context Breakout](book2/javascript-string-breakout.md)
- [Malformed Boolean-Attribute Sanitizer Bypass](book2/malformed-boolean-attribute-sanitizer-bypass.md)
- [Self-XSS Chaining with Login/Logout CSRF](book2/self-xss-chain-login-csrf.md)
- [Stored XSS Across Secondary Render Locations](book2/stored-xss-multi-render-location.md)
- [XSS Attribute Breakout with `autofocus` + `onfocus`](book2/html-attribute-breakout-autofocus.md)
- [XSS Filter Bypass with `document.writeln` + URL Fragment](book2/document-writeln-location-hash-bypass.md)
- [XSS via Alternate Input Path](book2/alternate-input-path-sanitization-bypass.md)

#### Chapter 8

- [AngularJS CSTI Probe and Version Check](book2/angularjs-csti-probe-and-version.md)
- [AngularJS Sandbox Escape Testing](book2/angularjs-sandbox-escape.md)
- [Cross-Service SSTI via Email Rendering](book2/cross-service-ssti-email-render.md)
- [Jinja2 Introspection as SSTI Impact Proof](book2/jinja2-introspection-proof.md)
- [Rails Dynamic `render` Path Traversal](book2/rails-dynamic-render-path-traversal.md)
- [Rails ERB Dynamic Render Code Execution Probe](book2/rails-erb-render-rce-probe.md)
- [Smarty `{php}` Tag Code-Execution Proof](book2/smarty-php-tag-code-execution.md)
- [Smarty SSTI Error + Version Probe](book2/smarty-error-and-version-probe.md)
- [Smarty/PHP File-Read Chunking](book2/smarty-file-read-chunking.md)
- [SSTI Arithmetic Fingerprinting](book2/ssti-arithmetic-fingerprinting.md)

#### Chapter 9

- [Blind SQLi Character-by-Character Extraction](book2/blind-sqli-character-bruteforce.md)
- [Blind SQLi Database-Version Boolean Test](book2/blind-sqli-version-boolean.md)
- [Blind SQLi Python Automation Pattern](book2/blind-sqli-python-automation-pattern.md)
- [Blind SQLi via Result Differential](book2/blind-sqli-result-differential.md)
- [Drupal `IN` Placeholder SQLi Pattern](book2/drupal-in-placeholder-sqli.md)
- [SQLi Comment-Out Query Tail](book2/sqli-comment-tail-bypass.md)
- [SQLi Inside Base64-Encoded JSON](book2/sqli-base64-json-parameter.md)
- [SQLi Quote + Boolean Probe](book2/sqli-quote-and-boolean-probe.md)
- [SQLi via Array Parameter Structure Change](book2/sqli-array-parameter-structure-change.md)
- [Time-Based Blind SQLi with `sleep()`](book2/time-based-blind-sqli-sleep.md)

#### Chapter 10

- [Blind SSRF OOB DNS Exfiltration](book2/ssrf-oob-dns-exfiltration.md)
- [Blind SSRF Timing-Based Port Scan](book2/blind-ssrf-timing-port-scan.md)
- [SSRF AWS Metadata Hostname Probe](book2/aws-metadata-hostname-probe.md)
- [SSRF Extension Filter Bypass with Query Delimiter](book2/ssrf-extension-filter-bypass-query.md)
- [SSRF External-to-Internal Redirect Bypass](book2/external-to-internal-redirect-bypass.md)
- [SSRF GET vs POST Capability Check](book2/ssrf-get-vs-post-capability.md)
- [SSRF into Internal DNS](book2/internal-dns-ssrf.md)
- [SSRF Localhost Filter Bypass with Alternate IP Notation](book2/webhook-localhost-alternate-notation.md)
- [SSRF Response-to-XSS Chain](book2/ssrf-response-to-xss.md)
- [SSRF URL-Parameter Discovery](book2/ssrf-url-parameter-discovery.md)

#### Chapter 11

- [Blind XXE External Callback](book2/xxe-oob-external-callback.md)
- [Python SimpleHTTPServer as XXE Callback Listener](book2/python-simplehttpserver-oob-listener.md)
- [XXE by Preserving Native XML Structure](book2/xxe-preserve-native-xml-structure.md)
- [XXE External DTD File Exfiltration](book2/xxe-external-dtd-file-exfil.md)
- [XXE in Office Document Uploads](book2/xxe-office-docx-upload.md)
- [XXE Local File Read](book2/xxe-local-file-read.md)

#### Chapter 12

- [Arbitrary File Write to SSH `authorized_keys`](book2/arbitrary-file-write-ssh-authorized-keys.md)
- [Command Flag Injection After Shell Escaping](book2/command-flag-injection-after-escaping.md)
- [ImageMagick Delegate Command Injection](book2/imagemagick-delegate-command-injection.md)
- [ImageMagick Extension-Only Upload Bypass](book2/imagemagick-content-type-extension-bypass.md)
- [Netcat Callback Listener for RCE Proof](book2/netcat-http-callback-listener.md)
- [OS Command Injection via Semicolon](book2/os-command-injection-semicolon.md)
- [Path Traversal to Arbitrary File Write](book2/path-traversal-arbitrary-file-write.md)
- [PHP `call_user_func` Function Injection](book2/php-call-user-func-function-injection.md)
- [Public Repository Secret Recon with Gitrob](book2/gitrob-secret-key-recon.md)
- [Rails `secret_key_base` Cookie-Forgery Risk](book2/rails-secret-key-cookie-forgery-risk.md)
- [Rails Signed-Cookie Deserialization RCE](book2/rails-signed-cookie-deserialization-rce.md)
- [Subdomain + Port + Screenshot Recon Workflow](book2/subdomain-port-screenshot-workflow.md)
- [Unrestricted PHP Upload to Code Execution](book2/unrestricted-php-upload-rce.md)

#### Chapter 13

- [`memcpy()` Source/Destination Size Audit](book2/memcpy-source-destination-size-audit.md)
- [Buffer Overflow Length-Check Review](book2/buffer-overflow-length-check-review.md)
- [libcurl POST Buffer Read-Out-of-Bounds Pattern](book2/libcurl-post-buffer-read-oob.md)
- [Managed-Language Native Extension Overflow Hunting](book2/native-extension-overflow-hunting.md)
- [Read-Out-of-Bounds Length Mismatch](book2/read-out-of-bounds-heartbleed-pattern.md)

#### Chapter 14

- [Certificate Transparency Subdomain Enumeration](book2/certificate-transparency-subdomain-enum.md)
- [CNAME to Unregistered Domain Takeover](book2/unregistered-domain-cname-takeover.md)
- [Dangling CNAME Subdomain Takeover](book2/subdomain-takeover-dangling-cname.md)
- [Provider Error-Signature Takeover Testing](book2/provider-error-signature-takeover.md)
- [SendGrid Inbound Parse Domain Takeover](book2/sendgrid-inbound-parse-domain-takeover.md)
- [Subdomain Takeover Enumeration with KnockPy](book2/subdomain-takeover-knockpy.md)
- [Wildcard Certificate Hash Pivot with Censys](book2/wildcard-cert-censys-pivot.md)
- [Wildcard Third-Party Subdomain Override](book2/wildcard-third-party-subdomain-override.md)

#### Chapter 15

- [Background Job Condition-Swap Race](book2/background-job-condition-swap.md)
- [Concurrent Request Limit Bypass with Burp](book2/burp-concurrent-limit-bypass.md)
- [Email Change vs Verification Race](book2/email-change-verification-race.md)
- [Manual Two-Browser Race Test](book2/manual-two-browser-race.md)
- [Race Condition / TOCTOU Identification](book2/race-condition-toctou-identification.md)

#### Chapter 16

- [Hidden POST-Body IDOR Discovery](book2/hidden-post-body-id-discovery.md)
- [IDOR in Hidden Iframe Requests](book2/iframe-hidden-endpoint-idor.md)
- [IDOR Privilege Escalation via Account/Administration ID](book2/idor-privilege-escalation-via-admin-id.md)
- [IDOR Secret Leak to Account Takeover](book2/idor-secret-leak-to-account-takeover.md)
- [Sequential Numeric IDOR Enumeration](book2/simple-sequential-id-enumeration.md)
- [UUID IDOR with Two Controlled Accounts](book2/two-account-uuid-swap.md)
- [UUID Leakage Hunting for IDOR](book2/uuid-leak-hunting.md)

#### Chapter 17

- [OAuth `redirect_uri` Prefix Validation Bypass](book2/oauth-redirect-uri-prefix-bypass.md)
- [OAuth `state` CSRF Validation](book2/oauth-state-csrf-validation.md)
- [OAuth Custom Registration Default-Password Flaw](book2/oauth-custom-registration-default-password.md)
- [OAuth Forgotten Whitelisted Domain Takeover](book2/oauth-forgotten-whitelisted-domain-takeover.md)
- [OAuth-Like Redirect Bypass via URL Userinfo Parsing](book2/oauth-wreply-userinfo-parser-bypass.md)

#### Chapter 18

- [2FA OTP Account-Binding Test](book2/two-factor-otp-account-binding-test.md)
- [CIDR Scan for Exposed `phpinfo.php`](book2/phpinfo-cidr-wget-scan.md)
- [EyeWitness Subdomain Visual Triage](book2/eyewitness-subdomain-triage.md)
- [Feature-Interaction Metric Manipulation](book2/feature-interaction-metric-manipulation.md)
- [Frontend-Only Permission Enforcement](book2/frontend-only-permission-check.md)
- [Hidden Endpoint Discovery in JavaScript](book2/javascript-hidden-endpoint-discovery.md)
- [Nmap Full-Port Version Scan](book2/nmap-full-port-version-scan.md)
- [Rails Mass Assignment](book2/rails-mass-assignment.md)
- [S3 Bucket Name Permutation Fuzzing](book2/s3-bucket-name-permutation-fuzzing.md)
- [S3 Public-Write Permission Test](book2/s3-public-write-test-aws-cli.md)
- [Unauthenticated Memcache Service Check](book2/memcache-unauthenticated-service-check.md)
- [Web vs Mobile Security-Control Bypass](book2/web-vs-mobile-security-check-bypass.md)

#### Chapter 19

- [Burp Intruder Path Discovery](book2/burp-intruder-path-discovery.md)
- [Enumerating Subdomains of Subdomains](book2/subdomain-of-subdomain-enumeration.md)
- [Functionality-to-Vulnerability Mapping](book2/functionality-to-vulnerability-mapping.md)
- [Generic Injection Polyglot Probe](book2/generic-injection-polyglot-probe.md)
- [GitHub Repository Sensitive-Data Review](book2/github-repository-sensitive-data-review.md)
- [Gobuster File and Directory Discovery](book2/gobuster-content-discovery.md)
- [Google Dorking for Vulnerability-Relevant Parameters](book2/google-dork-vulnerable-parameters.md)
- [IP Outlier Prioritization](book2/ip-outlier-prioritization.md)
- [JavaScript File Change Monitoring](book2/javascript-file-change-monitoring.md)
- [Meg Multi-Host Path Discovery](book2/meg-multi-host-path-discovery.md)
- [Nmap + Masscan Port-Scanning Workflow](book2/nmap-masscan-port-workflow.md)
- [Retesting Previously Disclosed Bugs](book2/previous-bug-retest-methodology.md)
- [Screenshot-Based Visual Recon Triage](book2/screenshot-visual-triage.md)
- [SubFinder Subdomain Enumeration](book2/subfinder-subdomain-enumeration.md)
- [Technology-Stack-Driven Testing](book2/technology-stack-driven-testing.md)

## Book 3 — Hacking APIs — Breaking Web Application Programming Interfaces

**Author:** Corey J. Ball

### By Category

#### Miscellaneous

- [API Threat-Model Test Mode](book3/api-threat-model-test-mode.md) — Ch. 0 — Batch 1
- [HTTP Method Enumeration with OPTIONS](book3/http-options-method-enumeration.md) — Ch. 1 — Batch 1
- [API Documentation Attack-Surface Mapping](book3/api-documentation-attack-surface-mapping.md) — Ch. 2 — Batch 1
- [API Header Information Fingerprinting](book3/api-header-information-fingerprinting.md) — Ch. 2 — Batch 1
- [API Key Location Hunting](book3/api-key-location-hunting.md) — Ch. 2 — Batch 1
- [Basic Authentication Base64 Recognition](book3/basic-auth-base64-recognition.md) — Ch. 2 — Batch 1
- [API BOLA Object-ID Swap](book3/api-bola-object-id-swap.md) — Ch. 3 — Batch 1
- [API Excessive Data Exposure](book3/excessive-data-exposure.md) — Ch. 3 — Batch 1
- [API Information Disclosure Response Review](book3/information-disclosure-response-review.md) — Ch. 3 — Batch 1
- [API Mass Assignment via Hidden Properties](book3/api-mass-assignment-isadmin.md) — Ch. 3 — Batch 1
- [API Rate-Limit Enforcement Test](book3/api-rate-limit-enforcement-test.md) — Ch. 3 — Batch 1
- [API Response-Time Side-Channel Enumeration](book3/response-time-side-channel-enumeration.md) — Ch. 3 — Batch 1
- [API SQL Injection Error Probe](book3/api-sqli-error-probe.md) — Ch. 3 — Batch 1
- [API Token Entropy Analysis](book3/api-token-entropy-analysis.md) — Ch. 3 — Batch 1
- [API Trust-Assumption Testing](book3/api-trust-assumption-testing.md) — Ch. 3 — Batch 1
- [API Version and Development-Path Enumeration](book3/api-version-dev-path-enumeration.md) — Ch. 3 — Batch 1
- [BFLA Admin Endpoint Test](book3/bfla-admin-endpoint-test.md) — Ch. 3 — Batch 1
- [Password Reset / MFA Code Rate-Limit Test](book3/password-reset-mfa-rate-limit-test.md) — Ch. 3 — Batch 1
- [Amass API-Key-Enhanced Recon](book3/amass-api-key-enhanced-recon.md) — Ch. 4 — Batch 2
- [Arjun Hidden Parameter Discovery](book3/arjun-hidden-parameter-discovery.md) — Ch. 4 — Batch 2
- [Autorize Two-User Authorization Check](book3/burp-autorize-two-user-check.md) — Ch. 4 — Batch 2
- [Burp + FoxyProxy Interception Setup](book3/burp-foxyproxy-interception-setup.md) — Ch. 4 — Batch 2
- [Burp Intruder Attack Types](book3/burp-intruder-attack-types.md) — Ch. 4 — Batch 2
- [Burp Intruder Attack-Position Fuzzing](book3/burp-intruder-attack-position.md) — Ch. 4 — Batch 2
- [Burp Repeater Baseline Differential Testing](book3/burp-repeater-baseline-differential-testing.md) — Ch. 4 — Batch 2
- [Burp Sequencer Token Randomness Analysis](book3/burp-sequencer-token-randomness.md) — Ch. 4 — Batch 2
- [DevTools API Request Discovery](book3/devtools-api-request-discovery.md) — Ch. 4 — Batch 2
- [DevTools Source Secret and Endpoint Search](book3/devtools-source-secret-search.md) — Ch. 4 — Batch 2
- [Import API Specifications into Postman](book3/postman-import-api-specification.md) — Ch. 4 — Batch 2
- [Kiterunner API Endpoint Discovery](book3/kiterunner-api-endpoint-discovery.md) — Ch. 4 — Batch 2
- [Nikto API Surface Scan](book3/nikto-api-surface-scan.md) — Ch. 4 — Batch 2
- [Postman Collection Runner](book3/postman-collection-runner.md) — Ch. 4 — Batch 2
- [Postman Environment Variables for API Testing](book3/postman-environment-secret-variables.md) — Ch. 4 — Batch 2
- [Postman Response Tests](book3/postman-response-tests.md) — Ch. 4 — Batch 2
- [Proxy Postman Through Burp Suite](book3/postman-through-burp-proxy.md) — Ch. 4 — Batch 2
- [Wfuzz API Path Fuzzing](book3/wfuzz-api-path-fuzzing.md) — Ch. 4 — Batch 2
- [Wfuzz Numeric-Range BOLA Probe](book3/wfuzz-bola-numeric-range.md) — Ch. 4 — Batch 2
- [Damn Vulnerable GraphQL Lab Setup](book3/dvga-graphql-lab-setup.md) — Ch. 5 — Batch 2
- [Discover APIs Behind a Web GUI with Burp](book3/browser-burp-api-behind-gui.md) — Ch. 5 — Batch 2
- [Isolate a Vulnerable API Lab](book3/isolate-vulnerable-api-lab.md) — Ch. 5 — Batch 2
- [Netdiscover Local Lab Host Discovery](book3/netdiscover-lab-host-discovery.md) — Ch. 5 — Batch 2
- [Nmap Default Scripts + Service Enumeration](book3/nmap-default-scripts-service-enum.md) — Ch. 5 — Batch 2
- [OWASP Juice Shop API Lab Setup](book3/juice-shop-api-lab-setup.md) — Ch. 5 — Batch 2
- [Pixi Vulnerable API Lab Setup](book3/pixi-vulnerable-api-lab-setup.md) — Ch. 5 — Batch 2
- [API Passive Recon Workflow](book3/api-passive-recon-workflow.md) — Ch. 6 — Batch 2
- [GitHub API Secret History Review](book3/github-api-secret-history-review.md) — Ch. 6 — Batch 2
- [Gobuster API Directory Enumeration](book3/gobuster-api-directory-enumeration.md) — Ch. 6 — Batch 2
- [Google Dorks for API Secrets and Documentation](book3/google-dorks-api-secrets-docs.md) — Ch. 6 — Batch 2
- [JavaScript API Endpoint String Search](book3/javascript-api-endpoint-string-search.md) — Ch. 6 — Batch 2
- [Kiterunner Multi-Method API Scan](book3/kiterunner-multi-method-api-scan.md) — Ch. 6 — Batch 2
- [Kiterunner Request Replay](book3/kiterunner-request-replay.md) — Ch. 6 — Batch 2
- [Nmap All-Port API Discovery](book3/nmap-all-port-api-discovery.md) — Ch. 6 — Batch 2
- [OWASP ZAP API URI Crawling](book3/zap-api-uri-crawling.md) — Ch. 6 — Batch 2
- [Public API Directory OSINT](book3/api-directory-osint.md) — Ch. 6 — Batch 2
- [Verbose Authentication Header API Discovery](book3/burp-verbose-auth-header-api-discovery.md) — Ch. 6 — Batch 2
- [API Documentation Path Discovery](book3/api-documentation-path-discovery.md) — Ch. 7 — Batch 3
- [Authenticated Kiterunner Scan](book3/kiterunner-authenticated-scan.md) — Ch. 7 — Batch 3
- [Build a Postman Collection by Proxy](book3/postman-proxy-api-reverse-engineering.md) — Ch. 7 — Batch 3
- [Business Logic Testing from Documentation Warnings](book3/api-documentation-negative-rule-testing.md) — Ch. 7 — Batch 3
- [Debug Page Endpoint Disclosure](book3/debug-page-endpoint-disclosure.md) — Ch. 7 — Batch 3
- [Excessive Data Exposure with Collection Runner](book3/excessive-data-exposure-collection-runner.md) — Ch. 7 — Batch 3
- [Import and Review API Specifications](book3/api-specification-import-and-review.md) — Ch. 7 — Batch 3
- [Manual API Reverse Engineering with Postman](book3/postman-manual-api-reverse-engineering.md) — Ch. 7 — Batch 3
- [Plain-HTTP API Token Leak Check](book3/plain-http-token-leak-check.md) — Ch. 7 — Batch 3
- [Replay Kiterunner Results Through Burp](book3/kiterunner-replay-through-burp.md) — Ch. 7 — Batch 3
- [Resource Enumeration by Status-Code Differences](book3/status-code-resource-enumeration.md) — Ch. 7 — Batch 3
- [Save API Authentication Tokens as Variables](book3/save-api-auth-token-variable.md) — Ch. 7 — Batch 3
- [Three-Phase Administrative Endpoint Authorization Test](book3/admin-endpoint-three-phase-auth-test.md) — Ch. 7 — Batch 3
- [Username Enumeration via Verbose Login Errors](book3/username-enumeration-verbose-login-errors.md) — Ch. 7 — Batch 3
- [Base64 Authentication Payload Processing in Intruder](book3/base64-auth-payload-processing.md) — Ch. 8 — Batch 3
- [Burp Sequencer Live Token Capture](book3/burp-sequencer-live-token-capture.md) — Ch. 8 — Batch 3
- [Burp Sequencer Manual Token Analysis](book3/burp-sequencer-manual-token-analysis.md) — Ch. 8 — Batch 3
- [JWT `alg:none` Validation Test](book3/jwt-none-algorithm-attack.md) — Ch. 8 — Batch 3
- [JWT HMAC Secret Dictionary Crack](book3/jwt-secret-dictionary-crack.md) — Ch. 8 — Batch 3
- [JWT Recognition and Decoding](book3/jwt-recognition-and-decoding.md) — Ch. 8 — Batch 3
- [JWT RS256-to-HS256 Key Confusion](book3/jwt-rs256-hs256-key-confusion.md) — Ch. 8 — Batch 3
- [JWT_Tool Playbook Scan](book3/jwt-tool-playbook-scan.md) — Ch. 8 — Batch 3
- [OTP Brute Force with Burp Intruder](book3/otp-bruteforce-burp-intruder.md) — Ch. 8 — Batch 3
- [Password Spraying with Intruder Cluster Bomb](book3/password-spraying-cluster-bomb.md) — Ch. 8 — Batch 3
- [Predictable Token Partial Brute Force](book3/predictable-token-partial-bruteforce.md) — Ch. 8 — Batch 3
- [Wfuzz JSON Login Brute-Force Pattern](book3/wfuzz-json-login-bruteforce.md) — Ch. 8 — Batch 3
- [API Directory Traversal Fuzzing](book3/api-directory-traversal-fuzzing.md) — Ch. 9 — Batch 3
- [Deep Fuzzing with Burp Intruder Sniper](book3/burp-deep-fuzzing-sniper.md) — Ch. 9 — Batch 3
- [Expected-Format + Payload Validation Bypass](book3/expected-format-plus-payload-bypass.md) — Ch. 9 — Batch 3
- [Fuzzing Baseline and Anomaly Detection](book3/fuzzing-baseline-anomaly-detection.md) — Ch. 9 — Batch 3
- [Generic API Fuzz Input Set](book3/generic-api-fuzz-input-set.md) — Ch. 9 — Batch 3
- [HTTP Method Fuzzing with Wfuzz](book3/http-method-fuzzing-wfuzz.md) — Ch. 9 — Batch 3
- [Improper Assets Management via Version Fuzzing](book3/improper-assets-version-fuzzing.md) — Ch. 9 — Batch 3
- [Input Sanitization Bypass with Delimiter + Payload](book3/input-sanitization-null-delimiter-bypass.md) — Ch. 9 — Batch 3
- [Legacy API Version OTP Rate-Limit Bypass](book3/legacy-api-otp-rate-limit-bypass.md) — Ch. 9 — Batch 3
- [Wfuzz Deep JSON-Body Fuzzing](book3/wfuzz-deep-json-body-fuzzing.md) — Ch. 9 — Batch 3
- [Wide Fuzzing with Postman Collection Runner](book3/postman-wide-fuzzing.md) — Ch. 9 — Batch 3
- [A-B Testing for BOLA](book3/bola-ab-testing.md) — Ch. 10 — Batch 4
- [A-B-A Testing for BFLA](book3/bfla-aba-testing.md) — Ch. 10 — Batch 4
- [BFLA via HTTP Method Authorization Gap](book3/bfla-method-authorization-gap.md) — Ch. 10 — Batch 4
- [BOLA ID-Combination Testing](book3/bola-id-combination-testing.md) — Ch. 10 — Batch 4
- [BOLA Resource-ID Location Testing](book3/bola-resource-id-location-testing.md) — Ch. 10 — Batch 4
- [BOLA via Duplicate JSON Keys](book3/bola-duplicate-key-testing.md) — Ch. 10 — Batch 4
- [BOLA via Nested JSON Object](book3/bola-nested-object-bypass.md) — Ch. 10 — Batch 4
- [Burp Match-and-Replace Authorization Testing](book3/burp-match-replace-auth-testing.md) — Ch. 10 — Batch 4
- [Chain Excessive Data Exposure into BOLA](book3/bola-chain-excessive-data-id-leak.md) — Ch. 10 — Batch 4
- [GUID/UUID BOLA with Two Controlled Accounts](book3/guid-bola-two-account-test.md) — Ch. 10 — Batch 4
- [Low-Privilege Admin Action Test](book3/bfla-lowpriv-admin-action.md) — Ch. 10 — Batch 4
- [Postman Collection Token-Swap Authorization Test](book3/postman-token-swap-wide-auth-test.md) — Ch. 10 — Batch 4
- [Side-Channel BOLA Enumeration](book3/bola-side-channel-enumeration.md) — Ch. 10 — Batch 4
- [Arjun JSON Parameter Discovery for Mass Assignment](book3/arjun-json-parameter-discovery-mass-assignment.md) — Ch. 11 — Batch 4
- [Blind Mass Assignment Variable Fuzzing](book3/blind-mass-assignment-variable-fuzzing.md) — Ch. 11 — Batch 4
- [Mass Assignment + BFLA Chain](book3/mass-assignment-bfla-chain.md) — Ch. 11 — Batch 4
- [Mass Assignment into Organization/Tenant](book3/mass-assignment-organization-field.md) — Ch. 11 — Batch 4
- [Mass Assignment Variable Mining from Documentation](book3/mass-assignment-variable-mining-docs.md) — Ch. 11 — Batch 4
- [Mass Assignment Variable Reuse Across Endpoints](book3/mass-assignment-variable-reuse.md) — Ch. 11 — Batch 4
- [Mass Assignment via Registration Admin Flag](book3/mass-assignment-registration-admin.md) — Ch. 11 — Batch 4
- [Negative Price / Credit Business Logic Test](book3/negative-price-business-logic.md) — Ch. 11 — Batch 4
- [API Injection Point Mapping](book3/api-injection-point-mapping.md) — Ch. 12 — Batch 4
- [API SQLi Metacharacter Probe](book3/sqli-metacharacter-probe-api.md) — Ch. 12 — Batch 4
- [API-to-Frontend Stored XSS Testing](book3/api-stored-xss-sink-testing.md) — Ch. 12 — Batch 4
- [Cross-API Scripting (XAS)](book3/cross-api-scripting-third-party.md) — Ch. 12 — Batch 4
- [NoSQL Injection JSON-Boundary Troubleshooting](book3/nosqli-payload-troubleshooting-json-boundary.md) — Ch. 12 — Batch 4
- [NoSQL Operator Authentication Bypass](book3/nosqli-operator-auth-bypass.md) — Ch. 12 — Batch 4
- [OS Command Separator Fuzzing](book3/os-command-separator-fuzzing.md) — Ch. 12 — Batch 4
- [SQLmap Saved-Request Parameter Test](book3/sqlmap-saved-request-parameter-test.md) — Ch. 12 — Batch 4
- [SQLmap Targeted Data Dump](book3/sqlmap-targeted-dump.md) — Ch. 12 — Batch 4
- [Wfuzz Command Separator + Command Matrix](book3/wfuzz-command-separator-command-matrix.md) — Ch. 12 — Batch 4
- [API Rate-Limit Identification](book3/rate-limit-identification.md) — Ch. 13 — Batch 4
- [Burp Intruder Payload Processing for Evasion](book3/burp-payload-processing-evasion.md) — Ch. 13 — Batch 4
- [Nmap HTTP WAF Detection](book3/nmap-http-waf-detect.md) — Ch. 13 — Batch 4
- [Rate-Limit Origin-Header Spoofing Test](book3/rate-limit-origin-header-spoofing.md) — Ch. 13 — Batch 4
- [Rate-Limit Path Variant Test](book3/rate-limit-path-variant-bypass.md) — Ch. 13 — Batch 4
- [Rate-Limit User-Agent Rotation Test](book3/rate-limit-user-agent-rotation.md) — Ch. 13 — Batch 4
- [WAF Case-Switching Test](book3/waf-case-switching-bypass.md) — Ch. 13 — Batch 4
- [WAF Payload Encoding Test](book3/waf-url-encoding-bypass.md) — Ch. 13 — Batch 4
- [WAF/CDN Detection from Headers](book3/waf-header-detection.md) — Ch. 13 — Batch 4
- [WAF/Input-Filter String Terminator Test](book3/waf-string-terminator-bypass.md) — Ch. 13 — Batch 4
- [Wfuzz Encoder Payload Processing](book3/wfuzz-encoder-payload-processing.md) — Ch. 13 — Batch 4
- [Wfuzz Request Throttling](book3/wfuzz-rate-throttling.md) — Ch. 13 — Batch 4
- [GraphiQL Cookie Feature Toggle](book3/graphiql-cookie-feature-toggle.md) — Ch. 14 — Batch 5
- [GraphiQL Documentation Explorer Query Building](book3/graphiql-documentation-explorer-query-building.md) — Ch. 14 — Batch 5
- [GraphQL Endpoint Wordlist Discovery](book3/graphql-endpoint-wordlist-discovery.md) — Ch. 14 — Batch 5
- [GraphQL Error-Body Baseline](book3/graphql-error-body-baseline.md) — Ch. 14 — Batch 5
- [GraphQL Introspection Schema Enumeration](book3/graphql-introspection-schema-enumeration.md) — Ch. 14 — Batch 5
- [GraphQL Path Variable Command Injection](book3/graphql-path-variable-command-injection.md) — Ch. 14 — Batch 5
- [GraphQL Private Object Exposure via BOLA](book3/graphql-private-object-public-flag-bola.md) — Ch. 14 — Batch 5
- [GraphQL Request Reverse Engineering](book3/graphql-request-reverse-engineering.md) — Ch. 14 — Batch 5
- [GraphQL Sequential pID BOLA Test](book3/graphql-pid-bola-test.md) — Ch. 14 — Batch 5
- [GraphQL Variable Command-Injection Fuzzing](book3/graphql-variable-command-injection-fuzz.md) — Ch. 14 — Batch 5
- [InQL Schema and Operation Mapping](book3/inql-schema-and-operation-mapping.md) — Ch. 14 — Batch 5
- [Address Search Excessive Data Exposure](book3/usps-address-excessive-data-exposure.md) — Ch. 15 — Batch 5
- [BFF Proxy Path Traversal Signal](book3/starbucks-bff-proxy-path-traversal.md) — Ch. 15 — Batch 5
- [GraphQL Media-ID BOLA](book3/instagram-graphql-bola-media-id.md) — Ch. 15 — Batch 5
- [GraphQL Null-Token Authorization Check](book3/graphql-null-token-authorization-check.md) — Ch. 15 — Batch 5
- [ID-Based BOLA in User Detail APIs](book3/peloton-id-based-bola.md) — Ch. 15 — Batch 5
- [Internal API Enumeration from Response Differences](book3/starbucks-internal-api-enumeration-from-response-differences.md) — Ch. 15 — Batch 5
- [JavaScript Exposed API Key](book3/javascript-exposed-api-key.md) — Ch. 15 — Batch 5
- [Phone Number BOLA](book3/tmobile-phone-number-bola.md) — Ch. 15 — Batch 5
- [Public API Docs + Exposed Bearer Token Chain](book3/public-api-docs-plus-exposed-bearer-token.md) — Ch. 15 — Batch 5
- [Unauthenticated User Data Exposure](book3/peloton-unauthenticated-user-data.md) — Ch. 15 — Batch 5
- [Wildcard Search Data Exposure](book3/usps-wildcard-user-search.md) — Ch. 15 — Batch 5
- [API Active Recon Checklist](book3/api-active-recon-checklist.md) — Ch. A — Batch 5
- [API Authentication Testing Checklist](book3/api-authentication-checklist.md) — Ch. A — Batch 5
- [API Authorization Testing Checklist](book3/api-authorization-checklist.md) — Ch. A — Batch 5
- [API Fuzzing Checklist](book3/api-fuzzing-checklist.md) — Ch. A — Batch 5
- [API Hacking Master Checklist](book3/api-hacking-master-checklist.md) — Ch. A — Batch 5
- [API Injection Testing Checklist](book3/api-injection-checklist.md) — Ch. A — Batch 5
- [API Rate-Limit and Evasion Checklist](book3/api-rate-limit-evasion-checklist.md) — Ch. A — Batch 5

### By Chapter

#### Chapter 0

- [API Threat-Model Test Mode](book3/api-threat-model-test-mode.md)

#### Chapter 1

- [HTTP Method Enumeration with OPTIONS](book3/http-options-method-enumeration.md)

#### Chapter 2

- [API Documentation Attack-Surface Mapping](book3/api-documentation-attack-surface-mapping.md)
- [API Header Information Fingerprinting](book3/api-header-information-fingerprinting.md)
- [API Key Location Hunting](book3/api-key-location-hunting.md)
- [Basic Authentication Base64 Recognition](book3/basic-auth-base64-recognition.md)

#### Chapter 3

- [API BOLA Object-ID Swap](book3/api-bola-object-id-swap.md)
- [API Excessive Data Exposure](book3/excessive-data-exposure.md)
- [API Information Disclosure Response Review](book3/information-disclosure-response-review.md)
- [API Mass Assignment via Hidden Properties](book3/api-mass-assignment-isadmin.md)
- [API Rate-Limit Enforcement Test](book3/api-rate-limit-enforcement-test.md)
- [API Response-Time Side-Channel Enumeration](book3/response-time-side-channel-enumeration.md)
- [API SQL Injection Error Probe](book3/api-sqli-error-probe.md)
- [API Token Entropy Analysis](book3/api-token-entropy-analysis.md)
- [API Trust-Assumption Testing](book3/api-trust-assumption-testing.md)
- [API Version and Development-Path Enumeration](book3/api-version-dev-path-enumeration.md)
- [BFLA Admin Endpoint Test](book3/bfla-admin-endpoint-test.md)
- [Password Reset / MFA Code Rate-Limit Test](book3/password-reset-mfa-rate-limit-test.md)

#### Chapter 4

- [Amass API-Key-Enhanced Recon](book3/amass-api-key-enhanced-recon.md)
- [Arjun Hidden Parameter Discovery](book3/arjun-hidden-parameter-discovery.md)
- [Autorize Two-User Authorization Check](book3/burp-autorize-two-user-check.md)
- [Burp + FoxyProxy Interception Setup](book3/burp-foxyproxy-interception-setup.md)
- [Burp Intruder Attack Types](book3/burp-intruder-attack-types.md)
- [Burp Intruder Attack-Position Fuzzing](book3/burp-intruder-attack-position.md)
- [Burp Repeater Baseline Differential Testing](book3/burp-repeater-baseline-differential-testing.md)
- [Burp Sequencer Token Randomness Analysis](book3/burp-sequencer-token-randomness.md)
- [DevTools API Request Discovery](book3/devtools-api-request-discovery.md)
- [DevTools Source Secret and Endpoint Search](book3/devtools-source-secret-search.md)
- [Import API Specifications into Postman](book3/postman-import-api-specification.md)
- [Kiterunner API Endpoint Discovery](book3/kiterunner-api-endpoint-discovery.md)
- [Nikto API Surface Scan](book3/nikto-api-surface-scan.md)
- [Postman Collection Runner](book3/postman-collection-runner.md)
- [Postman Environment Variables for API Testing](book3/postman-environment-secret-variables.md)
- [Postman Response Tests](book3/postman-response-tests.md)
- [Proxy Postman Through Burp Suite](book3/postman-through-burp-proxy.md)
- [Wfuzz API Path Fuzzing](book3/wfuzz-api-path-fuzzing.md)
- [Wfuzz Numeric-Range BOLA Probe](book3/wfuzz-bola-numeric-range.md)

#### Chapter 5

- [Damn Vulnerable GraphQL Lab Setup](book3/dvga-graphql-lab-setup.md)
- [Discover APIs Behind a Web GUI with Burp](book3/browser-burp-api-behind-gui.md)
- [Isolate a Vulnerable API Lab](book3/isolate-vulnerable-api-lab.md)
- [Netdiscover Local Lab Host Discovery](book3/netdiscover-lab-host-discovery.md)
- [Nmap Default Scripts + Service Enumeration](book3/nmap-default-scripts-service-enum.md)
- [OWASP Juice Shop API Lab Setup](book3/juice-shop-api-lab-setup.md)
- [Pixi Vulnerable API Lab Setup](book3/pixi-vulnerable-api-lab-setup.md)

#### Chapter 6

- [API Passive Recon Workflow](book3/api-passive-recon-workflow.md)
- [GitHub API Secret History Review](book3/github-api-secret-history-review.md)
- [Gobuster API Directory Enumeration](book3/gobuster-api-directory-enumeration.md)
- [Google Dorks for API Secrets and Documentation](book3/google-dorks-api-secrets-docs.md)
- [JavaScript API Endpoint String Search](book3/javascript-api-endpoint-string-search.md)
- [Kiterunner Multi-Method API Scan](book3/kiterunner-multi-method-api-scan.md)
- [Kiterunner Request Replay](book3/kiterunner-request-replay.md)
- [Nmap All-Port API Discovery](book3/nmap-all-port-api-discovery.md)
- [OWASP ZAP API URI Crawling](book3/zap-api-uri-crawling.md)
- [Public API Directory OSINT](book3/api-directory-osint.md)
- [Verbose Authentication Header API Discovery](book3/burp-verbose-auth-header-api-discovery.md)

#### Chapter 7

- [API Documentation Path Discovery](book3/api-documentation-path-discovery.md)
- [Authenticated Kiterunner Scan](book3/kiterunner-authenticated-scan.md)
- [Build a Postman Collection by Proxy](book3/postman-proxy-api-reverse-engineering.md)
- [Business Logic Testing from Documentation Warnings](book3/api-documentation-negative-rule-testing.md)
- [Debug Page Endpoint Disclosure](book3/debug-page-endpoint-disclosure.md)
- [Excessive Data Exposure with Collection Runner](book3/excessive-data-exposure-collection-runner.md)
- [Import and Review API Specifications](book3/api-specification-import-and-review.md)
- [Manual API Reverse Engineering with Postman](book3/postman-manual-api-reverse-engineering.md)
- [Plain-HTTP API Token Leak Check](book3/plain-http-token-leak-check.md)
- [Replay Kiterunner Results Through Burp](book3/kiterunner-replay-through-burp.md)
- [Resource Enumeration by Status-Code Differences](book3/status-code-resource-enumeration.md)
- [Save API Authentication Tokens as Variables](book3/save-api-auth-token-variable.md)
- [Three-Phase Administrative Endpoint Authorization Test](book3/admin-endpoint-three-phase-auth-test.md)
- [Username Enumeration via Verbose Login Errors](book3/username-enumeration-verbose-login-errors.md)

#### Chapter 8

- [Base64 Authentication Payload Processing in Intruder](book3/base64-auth-payload-processing.md)
- [Burp Sequencer Live Token Capture](book3/burp-sequencer-live-token-capture.md)
- [Burp Sequencer Manual Token Analysis](book3/burp-sequencer-manual-token-analysis.md)
- [JWT `alg:none` Validation Test](book3/jwt-none-algorithm-attack.md)
- [JWT HMAC Secret Dictionary Crack](book3/jwt-secret-dictionary-crack.md)
- [JWT Recognition and Decoding](book3/jwt-recognition-and-decoding.md)
- [JWT RS256-to-HS256 Key Confusion](book3/jwt-rs256-hs256-key-confusion.md)
- [JWT_Tool Playbook Scan](book3/jwt-tool-playbook-scan.md)
- [OTP Brute Force with Burp Intruder](book3/otp-bruteforce-burp-intruder.md)
- [Password Spraying with Intruder Cluster Bomb](book3/password-spraying-cluster-bomb.md)
- [Predictable Token Partial Brute Force](book3/predictable-token-partial-bruteforce.md)
- [Wfuzz JSON Login Brute-Force Pattern](book3/wfuzz-json-login-bruteforce.md)

#### Chapter 9

- [API Directory Traversal Fuzzing](book3/api-directory-traversal-fuzzing.md)
- [Deep Fuzzing with Burp Intruder Sniper](book3/burp-deep-fuzzing-sniper.md)
- [Expected-Format + Payload Validation Bypass](book3/expected-format-plus-payload-bypass.md)
- [Fuzzing Baseline and Anomaly Detection](book3/fuzzing-baseline-anomaly-detection.md)
- [Generic API Fuzz Input Set](book3/generic-api-fuzz-input-set.md)
- [HTTP Method Fuzzing with Wfuzz](book3/http-method-fuzzing-wfuzz.md)
- [Improper Assets Management via Version Fuzzing](book3/improper-assets-version-fuzzing.md)
- [Input Sanitization Bypass with Delimiter + Payload](book3/input-sanitization-null-delimiter-bypass.md)
- [Legacy API Version OTP Rate-Limit Bypass](book3/legacy-api-otp-rate-limit-bypass.md)
- [Wfuzz Deep JSON-Body Fuzzing](book3/wfuzz-deep-json-body-fuzzing.md)
- [Wide Fuzzing with Postman Collection Runner](book3/postman-wide-fuzzing.md)

#### Chapter 10

- [A-B Testing for BOLA](book3/bola-ab-testing.md)
- [A-B-A Testing for BFLA](book3/bfla-aba-testing.md)
- [BFLA via HTTP Method Authorization Gap](book3/bfla-method-authorization-gap.md)
- [BOLA ID-Combination Testing](book3/bola-id-combination-testing.md)
- [BOLA Resource-ID Location Testing](book3/bola-resource-id-location-testing.md)
- [BOLA via Duplicate JSON Keys](book3/bola-duplicate-key-testing.md)
- [BOLA via Nested JSON Object](book3/bola-nested-object-bypass.md)
- [Burp Match-and-Replace Authorization Testing](book3/burp-match-replace-auth-testing.md)
- [Chain Excessive Data Exposure into BOLA](book3/bola-chain-excessive-data-id-leak.md)
- [GUID/UUID BOLA with Two Controlled Accounts](book3/guid-bola-two-account-test.md)
- [Low-Privilege Admin Action Test](book3/bfla-lowpriv-admin-action.md)
- [Postman Collection Token-Swap Authorization Test](book3/postman-token-swap-wide-auth-test.md)
- [Side-Channel BOLA Enumeration](book3/bola-side-channel-enumeration.md)

#### Chapter 11

- [Arjun JSON Parameter Discovery for Mass Assignment](book3/arjun-json-parameter-discovery-mass-assignment.md)
- [Blind Mass Assignment Variable Fuzzing](book3/blind-mass-assignment-variable-fuzzing.md)
- [Mass Assignment + BFLA Chain](book3/mass-assignment-bfla-chain.md)
- [Mass Assignment into Organization/Tenant](book3/mass-assignment-organization-field.md)
- [Mass Assignment Variable Mining from Documentation](book3/mass-assignment-variable-mining-docs.md)
- [Mass Assignment Variable Reuse Across Endpoints](book3/mass-assignment-variable-reuse.md)
- [Mass Assignment via Registration Admin Flag](book3/mass-assignment-registration-admin.md)
- [Negative Price / Credit Business Logic Test](book3/negative-price-business-logic.md)

#### Chapter 12

- [API Injection Point Mapping](book3/api-injection-point-mapping.md)
- [API SQLi Metacharacter Probe](book3/sqli-metacharacter-probe-api.md)
- [API-to-Frontend Stored XSS Testing](book3/api-stored-xss-sink-testing.md)
- [Cross-API Scripting (XAS)](book3/cross-api-scripting-third-party.md)
- [NoSQL Injection JSON-Boundary Troubleshooting](book3/nosqli-payload-troubleshooting-json-boundary.md)
- [NoSQL Operator Authentication Bypass](book3/nosqli-operator-auth-bypass.md)
- [OS Command Separator Fuzzing](book3/os-command-separator-fuzzing.md)
- [SQLmap Saved-Request Parameter Test](book3/sqlmap-saved-request-parameter-test.md)
- [SQLmap Targeted Data Dump](book3/sqlmap-targeted-dump.md)
- [Wfuzz Command Separator + Command Matrix](book3/wfuzz-command-separator-command-matrix.md)

#### Chapter 13

- [API Rate-Limit Identification](book3/rate-limit-identification.md)
- [Burp Intruder Payload Processing for Evasion](book3/burp-payload-processing-evasion.md)
- [Nmap HTTP WAF Detection](book3/nmap-http-waf-detect.md)
- [Rate-Limit Origin-Header Spoofing Test](book3/rate-limit-origin-header-spoofing.md)
- [Rate-Limit Path Variant Test](book3/rate-limit-path-variant-bypass.md)
- [Rate-Limit User-Agent Rotation Test](book3/rate-limit-user-agent-rotation.md)
- [WAF Case-Switching Test](book3/waf-case-switching-bypass.md)
- [WAF Payload Encoding Test](book3/waf-url-encoding-bypass.md)
- [WAF/CDN Detection from Headers](book3/waf-header-detection.md)
- [WAF/Input-Filter String Terminator Test](book3/waf-string-terminator-bypass.md)
- [Wfuzz Encoder Payload Processing](book3/wfuzz-encoder-payload-processing.md)
- [Wfuzz Request Throttling](book3/wfuzz-rate-throttling.md)

#### Chapter 14

- [GraphiQL Cookie Feature Toggle](book3/graphiql-cookie-feature-toggle.md)
- [GraphiQL Documentation Explorer Query Building](book3/graphiql-documentation-explorer-query-building.md)
- [GraphQL Endpoint Wordlist Discovery](book3/graphql-endpoint-wordlist-discovery.md)
- [GraphQL Error-Body Baseline](book3/graphql-error-body-baseline.md)
- [GraphQL Introspection Schema Enumeration](book3/graphql-introspection-schema-enumeration.md)
- [GraphQL Path Variable Command Injection](book3/graphql-path-variable-command-injection.md)
- [GraphQL Private Object Exposure via BOLA](book3/graphql-private-object-public-flag-bola.md)
- [GraphQL Request Reverse Engineering](book3/graphql-request-reverse-engineering.md)
- [GraphQL Sequential pID BOLA Test](book3/graphql-pid-bola-test.md)
- [GraphQL Variable Command-Injection Fuzzing](book3/graphql-variable-command-injection-fuzz.md)
- [InQL Schema and Operation Mapping](book3/inql-schema-and-operation-mapping.md)

#### Chapter 15

- [Address Search Excessive Data Exposure](book3/usps-address-excessive-data-exposure.md)
- [BFF Proxy Path Traversal Signal](book3/starbucks-bff-proxy-path-traversal.md)
- [GraphQL Media-ID BOLA](book3/instagram-graphql-bola-media-id.md)
- [GraphQL Null-Token Authorization Check](book3/graphql-null-token-authorization-check.md)
- [ID-Based BOLA in User Detail APIs](book3/peloton-id-based-bola.md)
- [Internal API Enumeration from Response Differences](book3/starbucks-internal-api-enumeration-from-response-differences.md)
- [JavaScript Exposed API Key](book3/javascript-exposed-api-key.md)
- [Phone Number BOLA](book3/tmobile-phone-number-bola.md)
- [Public API Docs + Exposed Bearer Token Chain](book3/public-api-docs-plus-exposed-bearer-token.md)
- [Unauthenticated User Data Exposure](book3/peloton-unauthenticated-user-data.md)
- [Wildcard Search Data Exposure](book3/usps-wildcard-user-search.md)

#### Chapter A

- [API Active Recon Checklist](book3/api-active-recon-checklist.md)
- [API Authentication Testing Checklist](book3/api-authentication-checklist.md)
- [API Authorization Testing Checklist](book3/api-authorization-checklist.md)
- [API Fuzzing Checklist](book3/api-fuzzing-checklist.md)
- [API Hacking Master Checklist](book3/api-hacking-master-checklist.md)
- [API Injection Testing Checklist](book3/api-injection-checklist.md)
- [API Rate-Limit and Evasion Checklist](book3/api-rate-limit-evasion-checklist.md)

## Book 4 — Web Application Security, 2nd Edition

**Author:** Andrew Hoffman

### By Category

#### Miscellaneous

- [Functional + Technical Recon Model](book4/recon-functional-business-model.md) — Ch. 2 — Batch 1
- [Hidden Privileged API Inference](book4/hidden-privileged-api-inference.md) — Ch. 2 — Batch 1
- [JSON-Style Recon Mapping](book4/web-application-map-json.md) — Ch. 2 — Batch 1
- [RBAC Role Mapping During Recon](book4/rbac-role-mapping.md) — Ch. 2 — Batch 1
- [Recon Note Relationship Preservation](book4/recon-note-relationship-preservation.md) — Ch. 2 — Batch 1
- [Arrow Function Context Review](book4/arrow-function-context-review.md) — Ch. 3 — Batch 1
- [Asynchronous Order Security Review](book4/asynchronous-order-security-review.md) — Ch. 3 — Batch 1
- [Authentication vs Authorization Map](book4/authentication-vs-authorization-map.md) — Ch. 3 — Batch 1
- [Browser DOM Security Surface Mapping](book4/dom-security-surface-mapping.md) — Ch. 3 — Batch 1
- [CDN and Cache Security Mapping](book4/cdn-cache-security-mapping.md) — Ch. 3 — Batch 1
- [Centralized vs Per-Endpoint Authorization Signal](book4/centralized-authorization-signal.md) — Ch. 3 — Batch 1
- [Git History Secret Recon](book4/git-history-secret-recon.md) — Ch. 3 — Batch 1
- [GraphQL Capability Recon](book4/graphql-capability-recon.md) — Ch. 3 — Batch 1
- [HTTP Basic Authentication Identification](book4/basic-authentication-identification.md) — Ch. 3 — Batch 1
- [IndexedDB Recon](book4/indexeddb-recon.md) — Ch. 3 — Batch 1
- [JavaScript `var` Function-Scope Review](book4/var-function-scope-review.md) — Ch. 3 — Batch 1
- [JavaScript Function Context Analysis](book4/function-context-analysis.md) — Ch. 3 — Batch 1
- [JavaScript Global Variable Exposure](book4/global-variable-window-exposure.md) — Ch. 3 — Batch 1
- [JSON Rapid Parsing for Recon](book4/json-rapid-parsing-recon.md) — Ch. 3 — Batch 1
- [Local Storage Sensitive Data Review](book4/local-storage-sensitive-data-review.md) — Ch. 3 — Batch 1
- [Modern Multi-Application Architecture Model](book4/modern-multi-application-model.md) — Ch. 3 — Batch 1
- [Multiple Database Attack Surface](book4/multiple-database-attack-surface.md) — Ch. 3 — Batch 1
- [OAuth Trust-Boundary Recon](book4/oauth-trust-boundary-recon.md) — Ch. 3 — Batch 1
- [Prototype Pollution Recon Signal](book4/prototype-pollution-signal.md) — Ch. 3 — Batch 1
- [REST Resource + HTTP Verb Inference](book4/rest-resource-verb-inference.md) — Ch. 3 — Batch 1
- [REST Stateless Token Model](book4/rest-stateless-token-model.md) — Ch. 3 — Batch 1
- [Session Storage Sensitive Data Review](book4/session-storage-sensitive-data-review.md) — Ch. 3 — Batch 1
- [SPA Framework Detection](book4/spa-framework-detection.md) — Ch. 3 — Batch 1
- [Swagger/OpenAPI Documentation Discovery](book4/swagger-documentation-discovery.md) — Ch. 3 — Batch 1
- [Version Control as a Security Boundary](book4/vcs-security-boundary.md) — Ch. 3 — Batch 1
- [Affiliated Domain Discovery via Browser Network](book4/browser-network-affiliated-domain-discovery.md) — Ch. 4 — Batch 1
- [Asynchronous DNS Resolution Enumeration](book4/async-dns-resolution-enumeration.md) — Ch. 4 — Batch 1
- [Dictionary-Based Subdomain Enumeration](book4/dictionary-subdomain-attack.md) — Ch. 4 — Batch 1
- [DNS Zone Transfer Misconfiguration Test](book4/dns-zone-transfer-test.md) — Ch. 4 — Batch 1
- [Google `site:` + `-inurl:` Subdomain Discovery](book4/google-site-minus-inurl-subdomains.md) — Ch. 4 — Batch 1
- [Historical Archive URL Discovery](book4/archive-historical-url-discovery.md) — Ch. 4 — Batch 1
- [Network Timing Side-Channel Signal](book4/network-timing-side-channel-signal.md) — Ch. 4 — Batch 1
- [Public Record Secret Discovery](book4/public-record-secret-discovery.md) — Ch. 4 — Batch 1
- [Social Media Subdomain OSINT](book4/social-media-subdomain-osint.md) — Ch. 4 — Batch 1
- [Subdomain Brute Force as Last Resort](book4/subdomain-bruteforce-last-resort.md) — Ch. 4 — Batch 1
- [XHR/Fetch API Endpoint Discovery](book4/xhr-api-endpoint-discovery.md) — Ch. 4 — Batch 1
- [Application-Specific Payload Shape Inference](book4/application-specific-payload-shape-inference.md) — Ch. 5 — Batch 2
- [Bearer Token as REST Stateless Signal](book4/rest-bearer-token-stateless-signal.md) — Ch. 5 — Batch 2
- [HTTP Verb Enumeration](book4/http-verb-enumeration.md) — Ch. 5 — Batch 2
- [OPTIONS Method Discovery](book4/options-method-discovery.md) — Ch. 5 — Batch 2
- [Payload Solutions-Space Reduction](book4/solutions-space-reduction.md) — Ch. 5 — Batch 2
- [REST Endpoint Pattern Recognition](book4/rest-endpoint-pattern-recognition.md) — Ch. 5 — Batch 2
- [Verbose Error Payload-Shape Disclosure](book4/verbose-error-shape-disclosure.md) — Ch. 5 — Batch 2
- [Angular Version Detection](book4/angular-version-detection.md) — Ch. 6 — Batch 2
- [CSS Library Inventory](book4/css-library-inventory.md) — Ch. 6 — Batch 2
- [Default 404 Fingerprinting](book4/default-404-fingerprinting.md) — Ch. 6 — Batch 2
- [EmberJS Detection](book4/emberjs-detection.md) — Ch. 6 — Batch 2
- [External JavaScript Script Inventory](book4/javascript-external-script-inventory.md) — Ch. 6 — Batch 2
- [MongoDB ObjectId Fingerprinting](book4/mongodb-objectid-fingerprinting.md) — Ch. 6 — Batch 2
- [Primary-Key Database Detection](book4/primary-key-database-detection.md) — Ch. 6 — Batch 2
- [Rails 404 Version-Range Fingerprinting](book4/rails-404-version-range-fingerprinting.md) — Ch. 6 — Batch 2
- [React Version Detection](book4/react-version-detection.md) — Ch. 6 — Batch 2
- [Server Detection via Response Headers](book4/x-powered-by-server-detection.md) — Ch. 6 — Batch 2
- [Third-Party Dependency Inventory](book4/third-party-dependency-inventory.md) — Ch. 6 — Batch 2
- [Vue Version Detection](book4/vue-version-detection.md) — Ch. 6 — Batch 2
- [Centralized DOM Sanitization Signal](book4/centralized-dom-sanitization-signal.md) — Ch. 7 — Batch 2
- [Custom Cryptography Risk Signal](book4/custom-crypto-risk-signal.md) — Ch. 7 — Batch 2
- [Security Layer Count Prioritization](book4/security-layer-count-prioritization.md) — Ch. 7 — Batch 2
- [Security-by-Design vs Feature-Time Security](book4/security-by-design-vs-feature-time.md) — Ch. 7 — Batch 2
- [Weakest-Link Layer Analysis](book4/weakest-link-layer-analysis.md) — Ch. 7 — Batch 2
- [Recon Technique Versioning](book4/recon-technique-versioning.md) — Ch. 8 — Batch 2
- [Applied Recon to Offense Transition](book4/applied-recon-to-offense.md) — Ch. 9 — Batch 2
- [`document.write()` XSS Sink](book4/document-write-sink.md) — Ch. 10 — Batch 2
- [`innerHTML` XSS Sink](book4/innerhtml-sink.md) — Ch. 10 — Batch 2
- [`window.location.hash` as XSS Source](book4/location-hash-source.md) — Ch. 10 — Batch 2
- [Browser Tag Auto-Closure Bypass Signal](book4/self-closing-tag-filter-bypass-signal.md) — Ch. 10 — Batch 2
- [DOM XSS Source/Sink Model](book4/dom-source-sink-model.md) — Ch. 10 — Batch 2
- [HTML Rendering as an XSS Signal](book4/html-rendering-as-xss-signal.md) — Ch. 10 — Batch 2
- [Malformed Tag Parser Repair](book4/malformed-tag-parser-repair.md) — Ch. 10 — Batch 2
- [Mutation-Based XSS Signal](book4/mutation-xss-signal.md) — Ch. 10 — Batch 2
- [Protocol-Relative URL Filter Bypass Signal](book4/protocol-relative-url-filter-bypass-signal.md) — Ch. 10 — Batch 2
- [Reflected Query-Parameter XSS](book4/reflected-query-param-xss.md) — Ch. 10 — Batch 2
- [Reflected XSS Link Delivery](book4/reflected-xss-link-delivery.md) — Ch. 10 — Batch 2
- [Stored XSS Against Privileged Viewers](book4/stored-xss-privileged-viewer-risk.md) — Ch. 10 — Batch 2
- [Stored XSS Data Flow](book4/stored-xss-data-flow.md) — Ch. 10 — Batch 2
- [Unicode Encoding Filter-Bypass Signal](book4/unicode-encoding-filter-bypass-signal.md) — Ch. 10 — Batch 2
- [XSS Polyglot Context Testing](book4/polyglot-context-testing.md) — Ch. 10 — Batch 2
- [XSS Sink Inventory](book4/xss-sink-inventory.md) — Ch. 10 — Batch 2
- [XSS Source Inventory](book4/xss-source-inventory.md) — Ch. 10 — Batch 2
- [Cross-User CSRF Token Reuse](book4/token-pool-cross-user-reuse.md) — Ch. 11 — Batch 3
- [CSRF Content-Type Validation Gap](book4/content-type-validation-gap.md) — Ch. 11 — Batch 3
- [CSRF Regex URL Validator Bypass Signal](book4/regex-url-validator-bypass-signal.md) — Ch. 11 — Batch 3
- [Iframe GET CSRF](book4/iframe-get-csrf.md) — Ch. 11 — Batch 3
- [Image-Source GET CSRF](book4/image-src-get-csrf.md) — Ch. 11 — Batch 3
- [POST Form CSRF](book4/form-post-csrf.md) — Ch. 11 — Batch 3
- [Predictable CSRF Token Analysis](book4/predictable-token-analysis.md) — Ch. 11 — Batch 3
- [Referrer/Origin Validation Bypass Signal](book4/referrer-origin-null-bypass-signal.md) — Ch. 11 — Batch 3
- [State-Changing GET CSRF](book4/get-state-change-csrf.md) — Ch. 11 — Batch 3
- [Zero-Interaction Form Submission](book4/zero-interaction-form-submit.md) — Ch. 11 — Batch 3
- [Blind XXE Out-of-Band Detection](book4/oob-callback-detection.md) — Ch. 12 — Batch 3
- [Direct XXE File-Read Test](book4/direct-external-entity-read.md) — Ch. 12 — Batch 3
- [Indirect JSON-to-XML XXE Signal](book4/indirect-json-to-xml-conversion.md) — Ch. 12 — Batch 3
- [XML-Like Input Discovery](book4/xml-like-input-discovery.md) — Ch. 12 — Batch 3
- [XML-to-Image Parser Chain](book4/xml-to-image-parser-chain.md) — Ch. 12 — Batch 3
- [XXE Linux Account-File Risk Chain](book4/linux-account-file-risk-chain.md) — Ch. 12 — Batch 3
- [XXE Password-Hash Escalation Risk](book4/hash-cracking-risk-documentation.md) — Ch. 12 — Batch 3
- [Authentication Query Injection Risk](book4/sql-auth-query-risk.md) — Ch. 13 — Batch 3
- [Blind Time-Delay Injection Detection](book4/blind-time-delay-detection.md) — Ch. 13 — Batch 3
- [CLI Code Injection Signal](book4/cli-code-injection-signal.md) — Ch. 13 — Batch 3
- [Filename-to-CLI Injection Signal](book4/filename-to-cli-injection.md) — Ch. 13 — Batch 3
- [In-Band Injection Result Detection](book4/in-band-exfiltration.md) — Ch. 13 — Batch 3
- [Injection Blocklist Encoding Bypass Signal](book4/blocklist-encoding-bypass-signal.md) — Ch. 13 — Batch 3
- [OS Command Concatenation Signal](book4/os-command-concatenation-signal.md) — Ch. 13 — Batch 3
- [Out-of-Band Injection Callback Risk](book4/oob-exfiltration-risk.md) — Ch. 13 — Batch 3
- [SQL String Concatenation Signal](book4/sql-string-concatenation-signal.md) — Ch. 13 — Batch 3
- [Autoscaling Cost-Abuse Risk](book4/autoscaling-cost-risk.md) — Ch. 14 — Batch 3
- [Endpoint Scaling by Account Archetype](book4/scaling-by-account-archetype.md) — Ch. 14 — Batch 3
- [File Compression DoS Risk](book4/file-compression-dos-risk.md) — Ch. 14 — Batch 3
- [ReDoS Catastrophic Backtracking](book4/redos-catastrophic-backtracking.md) — Ch. 14 — Batch 3
- [Resource-Intensive Endpoint Mapping](book4/resource-intensive-endpoint-mapping.md) — Ch. 14 — Batch 3
- [File IDOR via Direct Filename Reference](book4/file-id-direct-reference.md) — Ch. 15 — Batch 3
- [Mass Assignment Role Escalation](book4/mass-assignment-role-escalation.md) — Ch. 15 — Batch 3
- [Mass Assignment via Extra Object Fields](book4/mass-assignment-extra-fields.md) — Ch. 15 — Batch 3
- [Serializer Identification](book4/serializer-identification.md) — Ch. 15 — Batch 3
- [Weak Serializer Code-Execution Signal](book4/weak-serializer-code-execution-signal.md) — Ch. 15 — Batch 3
- [`target=_blank` Tabnabbing Signal](book4/target-blank-tabnabbing-signal.md) — Ch. 16 — Batch 3
- [Clickjacking Framing Signal](book4/clickjacking-framing-signal.md) — Ch. 16 — Batch 3
- [Iframe Parent Navigation Risk](book4/iframe-parent-navigation-risk.md) — Ch. 16 — Batch 3
- [Prototype Pollution Property Injection](book4/prototype-pollution-property-injection.md) — Ch. 16 — Batch 3
- [Prototype Pollution to Code-Execution Sink](book4/prototype-pollution-to-code-exec-sink.md) — Ch. 16 — Batch 3
- [Prototype Pollution via Unsafe Merge](book4/prototype-pollution-merge-signal.md) — Ch. 16 — Batch 3
- [Reverse Tabnabbing via `window.opener`](book4/reverse-tabnabbing-window-opener.md) — Ch. 16 — Batch 3
- [Branch vs Fork Integration Risk](book4/branch-vs-fork-risk.md) — Ch. 17 — Batch 4
- [Dependency CVE Cross-Reference](book4/cve-version-cross-reference.md) — Ch. 17 — Batch 4
- [Direct Source Integration Risk](book4/direct-source-integration-risk.md) — Ch. 17 — Batch 4
- [Malicious Transitive Package Risk](book4/malicious-transitive-package-risk.md) — Ch. 17 — Batch 4
- [npm Manifest Detection](book4/npm-manifest-detection.md) — Ch. 17 — Batch 4
- [OSS Integration Risk Mapping](book4/oss-integration-risk-mapping.md) — Ch. 17 — Batch 4
- [Package Maintainer Account Compromise Risk](book4/maintainer-account-compromise-risk.md) — Ch. 17 — Batch 4
- [Self-Hosted Installer Risk](book4/self-hosted-installer-risk.md) — Ch. 17 — Batch 4
- [Transitive Dependency Risk](book4/package-manager-transitive-risk.md) — Ch. 17 — Batch 4
- [IEEE754 Financial Precision Risk](book4/ieee754-financial-precision.md) — Ch. 18 — Batch 4
- [Intended vs Programmed Business Rules](book4/intended-vs-programmed-rules.md) — Ch. 18 — Batch 4
- [Local vs Global Price Validation](book4/local-vs-global-price-validation.md) — Ch. 18 — Batch 4
- [Missing Balance Validation](book4/missing-balance-validation.md) — Ch. 18 — Batch 4
- [Negative Numeric Edge Case](book4/negative-value-edge-case.md) — Ch. 18 — Batch 4
- [Programmed Side-Effect Abuse](book4/side-effect-abuse.md) — Ch. 18 — Batch 4
- [Quasi-Cash Reward Loop](book4/quasi-cash-reward-loop.md) — Ch. 18 — Batch 4
- [Refund + Reward Retention Check](book4/refund-reward-retention.md) — Ch. 18 — Batch 4
- [Use-Case Edge-Case Modeling](book4/use-case-edge-case-modeling.md) — Ch. 18 — Batch 4
- [Live Offensive Testing Safety](book4/offense-live-testing-safety.md) — Ch. 19 — Batch 4
- [Cross-Team Security Review](book4/cross-team-security-review.md) — Ch. 20 — Batch 4
- [Proactive Vulnerability Discovery Program](book4/proactive-vulnerability-discovery.md) — Ch. 20 — Batch 4
- [Risk-Based Vulnerability Prioritization](book4/risk-based-vulnerability-prioritization.md) — Ch. 20 — Batch 4
- [Secure Architecture First](book4/secure-architecture-first.md) — Ch. 20 — Batch 4
- [Security Code Review Four-Question Baseline](book4/security-code-review-four-questions.md) — Ch. 20 — Batch 4
- [Temporary Monitoring During Remediation](book4/temporary-monitoring-during-remediation.md) — Ch. 20 — Batch 4
- [Vulnerability Management Workflow](book4/vulnerability-management-workflow.md) — Ch. 20 — Batch 4
- [Vulnerability Regression Testing](book4/vulnerability-regression-testing.md) — Ch. 20 — Batch 4
- [BCrypt Password Storage](book4/bcrypt-password-storage.md) — Ch. 21 — Batch 4
- [Continuous Authorization After Role Change](book4/continuous-authorization-state-change.md) — Ch. 21 — Batch 4
- [Data-in-Transit Encryption Requirement](book4/data-in-transit-encryption.md) — Ch. 21 — Batch 4
- [Feature Requirement Security Review](book4/feature-requirement-security-review.md) — Ch. 21 — Batch 4
- [MFA Architecture](book4/mfa-architecture.md) — Ch. 21 — Batch 4
- [Password Entropy Policy](book4/password-entropy-policy.md) — Ch. 21 — Batch 4
- [Password Hashing Algorithm Selection](book4/password-hashing-choice.md) — Ch. 21 — Batch 4
- [PBKDF2 Password Storage](book4/pbkdf2-password-storage.md) — Ch. 21 — Batch 4
- [PII and Financial Data Minimization](book4/pii-financial-data-minimization.md) — Ch. 21 — Batch 4
- [Search Index Permission Synchronization](book4/search-index-permission-sync.md) — Ch. 21 — Batch 4
- [Zero Trust Explicit Verification](book4/zero-trust-explicit-verification.md) — Ch. 21 — Batch 4
- [`X-Content-Type-Options: nosniff`](book4/x-content-type-options-nosniff.md) — Ch. 22 — Batch 5
- [Cookie Domain Attribute Risk](book4/domain-attribute-risk.md) — Ch. 22 — Batch 5
- [Cookie Path Minimization](book4/cookie-path-minimization.md) — Ch. 22 — Batch 5
- [COOP `same-origin`](book4/coop-same-origin.md) — Ch. 22 — Batch 5
- [CORP Resource Isolation](book4/corp-same-origin.md) — Ch. 22 — Batch 5
- [CORS Preflight Model](book4/cors-preflight-model.md) — Ch. 22 — Batch 5
- [CORS Simple Request Model](book4/cors-simple-request-model.md) — Ch. 22 — Batch 5
- [CORS Wildcard Scope Risk](book4/cors-wildcard-risk.md) — Ch. 22 — Batch 5
- [CSP `default-src` Baseline](book4/csp-default-src.md) — Ch. 22 — Batch 4
- [CSP `frame-ancestors` Clickjacking Defense](book4/csp-frame-ancestors.md) — Ch. 22 — Batch 4
- [CSP `unsafe-inline` / `unsafe-eval` Risk](book4/csp-unsafe-inline-eval-risk.md) — Ch. 22 — Batch 4
- [CSP Delivery via Header or Meta](book4/csp-header-or-meta.md) — Ch. 22 — Batch 4
- [CSP Violation Reporting](book4/csp-reporting.md) — Ch. 22 — Batch 4
- [Hash-Based Strict CSP](book4/strict-csp-hash.md) — Ch. 22 — Batch 4
- [HSTS Enforcement](book4/hsts-enforcement.md) — Ch. 22 — Batch 5
- [HttpOnly Cookie Flag](book4/httponly-cookie-flag.md) — Ch. 22 — Batch 5
- [Iframe Sandbox Attribute](book4/iframe-sandbox-attribute.md) — Ch. 22 — Batch 5
- [Nonce-Based Strict CSP](book4/strict-csp-nonce.md) — Ch. 22 — Batch 4
- [Remove `X-Powered-By`](book4/x-powered-by-removal.md) — Ch. 22 — Batch 5
- [SameSite Strict Cookie](book4/samesite-strict.md) — Ch. 22 — Batch 5
- [Secure Cookie Flag](book4/secure-cookie-flag.md) — Ch. 22 — Batch 5
- [Subresource Integrity](book4/subresource-integrity.md) — Ch. 22 — Batch 5
- [Web Worker Isolation](book4/web-worker-isolation.md) — Ch. 22 — Batch 5
- [Authentication Enumeration Prevention](book4/authentication-enumeration-prevention.md) — Ch. 23 — Batch 5
- [Avoid Guessable Identifiers](book4/unguessable-identifiers.md) — Ch. 23 — Batch 5
- [Enumeration Rate Limits](book4/enumeration-rate-limits.md) — Ch. 23 — Batch 5
- [Generic User-Facing Error Messages](book4/generic-error-messages.md) — Ch. 23 — Batch 5
- [Security Light Patterns](book4/security-light-patterns.md) — Ch. 23 — Batch 5
- [Transaction Outflow Cap](book4/transaction-outflow-cap.md) — Ch. 23 — Batch 5
- [Attack Vector Cross-Analysis](book4/attack-vector-cross-analysis.md) — Ch. 24 — Batch 5
- [GraphQL Compute Limits](book4/graphql-compute-limits.md) — Ch. 24 — Batch 5
- [GraphQL Production Hardening](book4/graphql-production-hardening.md) — Ch. 24 — Batch 5
- [Internal Actor Worst-Case Modeling](book4/internal-actor-worst-case.md) — Ch. 24 — Batch 5
- [Privileged Token Scope Reduction](book4/privileged-token-scope.md) — Ch. 24 — Batch 5
- [Threat Actor Inventory](book4/threat-actor-inventory.md) — Ch. 24 — Batch 5
- [Threat Model Delta Identification](book4/delta-identification.md) — Ch. 24 — Batch 5
- [Threat Model Logic Design](book4/logic-design-document.md) — Ch. 24 — Batch 5
- [Threat Model Mitigation Inventory](book4/mitigation-inventory.md) — Ch. 24 — Batch 5
- [Threat Model Technical Design](book4/technical-design-document.md) — Ch. 24 — Batch 5
- [Archetype + Business Logic Review](book4/archetype-plus-business-logic.md) — Ch. 25 — Batch 5
- [Boilerplate Production Anti-Pattern](book4/boilerplate-production-antipattern.md) — Ch. 25 — Batch 5
- [Client-to-Server Security Review Path](book4/client-to-server-review-path.md) — Ch. 25 — Batch 5
- [Client/Server Coupling Anti-Pattern](book4/client-server-coupling-antipattern.md) — Ch. 25 — Batch 5
- [Local `git diff` Security Review Workflow](book4/local-git-diff-workflow.md) — Ch. 25 — Batch 5
- [Security Blocklist Anti-Pattern](book4/blocklist-antipattern.md) — Ch. 25 — Batch 5
- [Security Review at Merge](book4/security-review-at-merge.md) — Ch. 25 — Batch 5
- [Trust-by-Default Server Account Anti-Pattern](book4/trust-by-default-antipattern.md) — Ch. 25 — Batch 5
- [Bug Bounty as Discovery Layer](book4/bug-bounty-program-layer.md) — Ch. 26 — Batch 5
- [CSRF HTTP-Method Regression Test](book4/csrf-method-regression-test.md) — Ch. 26 — Batch 5
- [Dynamic Analysis Pipeline](book4/dynamic-analysis-pipeline.md) — Ch. 26 — Batch 5
- [Responsible Disclosure Program](book4/responsible-disclosure-program.md) — Ch. 26 — Batch 5
- [Security Regression Test Suite](book4/security-regression-tests.md) — Ch. 26 — Batch 5
- [Static Analysis Pipeline](book4/static-analysis-pipeline.md) — Ch. 26 — Batch 5
- [Static SQLi/CSRF/DoS Rule Patterns](book4/static-rule-sqli-csrf-dos.md) — Ch. 26 — Batch 5
- [Static XSS Rule Patterns](book4/static-rule-xss.md) — Ch. 26 — Batch 5
- [Third-Party Penetration Testing Focus](book4/third-party-pentest-focus.md) — Ch. 26 — Batch 5
- [Business-Aware Vulnerability Scoring](book4/custom-scoring-extension.md) — Ch. 27 — Batch 6
- [CVSS Attack Complexity](book4/cvss-attack-complexity.md) — Ch. 27 — Batch 6
- [CVSS Attack Vector](book4/cvss-attack-vector.md) — Ch. 27 — Batch 6
- [CVSS Base Scoring](book4/cvss-base-score.md) — Ch. 27 — Batch 6
- [CVSS Confidentiality/Integrity/Availability Impact](book4/cvss-cia-impact.md) — Ch. 27 — Batch 6
- [CVSS Environmental Scoring](book4/cvss-environmental.md) — Ch. 27 — Batch 6
- [CVSS Privileges + User Interaction](book4/cvss-privileges-user-interaction.md) — Ch. 27 — Batch 6
- [CVSS Temporal Scoring](book4/cvss-temporal.md) — Ch. 27 — Batch 6
- [Permanent vs Partial Security Fix](book4/permanent-vs-partial-fix.md) — Ch. 27 — Batch 6
- [Production-Like Vulnerability Reproduction](book4/staging-reproduction.md) — Ch. 27 — Batch 6
- [Regression Test Required on Closure](book4/regression-on-close.md) — Ch. 27 — Batch 6
- [Vulnerability Reproduction Logging](book4/reproduction-logging.md) — Ch. 27 — Batch 6
- [Centralized HTML Sanitization](book4/centralized-html-sanitization.md) — Ch. 28 — Batch 6
- [CSP Script Source Allowlist](book4/csp-script-src-allowlist.md) — Ch. 28 — Batch 6
- [Dangerous DOM Sink Reduction](book4/dangerous-dom-sink-removal.md) — Ch. 28 — Batch 6
- [DOMParser Safe Alternative](book4/domparser-safe-alternative.md) — Ch. 28 — Batch 6
- [HTML Entity Encoding](book4/html-entity-encoding.md) — Ch. 28 — Batch 6
- [Hyperlink Canonicalization](book4/hyperlink-canonicalization.md) — Ch. 28 — Batch 6
- [Prefer Text-Only DOM Insertion](book4/text-only-dom-insertion.md) — Ch. 28 — Batch 6
- [Remove Eval-Like Code Paths](book4/remove-eval-like-code.md) — Ch. 28 — Batch 6
- [SVG and Blob Script Risk](book4/svg-blob-risk.md) — Ch. 28 — Batch 6
- [User-Supplied CSS Risk](book4/user-css-risk.md) — Ch. 28 — Batch 6
- [Application-Wide Anti-CSRF Middleware](book4/application-wide-middleware.md) — Ch. 29 — Batch 6
- [No State Changes on GET](book4/no-state-change-on-get.md) — Ch. 29 — Batch 6
- [Origin + Referer CSRF Check](book4/origin-referer-check.md) — Ch. 29 — Batch 6
- [Session-Bound CSRF Token](book4/session-bound-csrf-token.md) — Ch. 29 — Batch 6
- [Stateless CSRF Token](book4/stateless-csrf-token.md) — Ch. 29 — Batch 6
- [Disable XML External Entities](book4/disable-external-entities.md) — Ch. 30 — Batch 6
- [Replace XML with Simpler Data Formats](book4/replace-xml-with-json.md) — Ch. 30 — Batch 6
- [XML Parser Egress Restriction](book4/parser-egress-restriction.md) — Ch. 30 — Batch 6
- [Database-Specific Escaping as Secondary Defense](book4/database-specific-escaping.md) — Ch. 31 — Batch 6
- [High-Risk Interpreter Inventory](book4/high-risk-interpreter-inventory.md) — Ch. 31 — Batch 6
- [Least Authority for Interpreter Modules](book4/least-authority-modules.md) — Ch. 31 — Batch 6
- [Prepared Statements as Primary SQLi Defense](book4/prepared-statements.md) — Ch. 31 — Batch 6
- [Server Command Allowlist](book4/command-allowlist.md) — Ch. 31 — Batch 6
- [SQL Query Inventory](book4/sql-query-inventory.md) — Ch. 31 — Batch 6
- [DDoS Bandwidth Management](book4/ddos-bandwidth-service.md) — Ch. 32 — Batch 6
- [DDoS Blackhole Routing](book4/blackhole-routing.md) — Ch. 32 — Batch 6
- [DoS Resource Risk Tiering](book4/resource-risk-tiering.md) — Ch. 32 — Batch 6
- [DoS-Oriented Request Performance Logging](book4/request-performance-logging.md) — Ch. 32 — Batch 6
- [Regex DoS Linting](book4/regex-linting.md) — Ch. 32 — Batch 6
- [Reject User-Supplied Regex](book4/no-user-supplied-regex.md) — Ch. 32 — Batch 6
- [Data Transfer Object Defense](book4/data-transfer-object-defense.md) — Ch. 33 — Batch 7
- [Mass Assignment Field Allowlist](book4/mass-assignment-field-allowlist.md) — Ch. 33 — Batch 7
- [Object Authorization Before Return](book4/object-authorization-before-return.md) — Ch. 33 — Batch 7
- [Random Object Reference as Defense-in-Depth](book4/random-object-reference-defense.md) — Ch. 33 — Batch 7
- [Serialization Type Allowlist](book4/serialization-type-allowlist.md) — Ch. 33 — Batch 7
- [Strong Serializer Library Selection](book4/strong-serializer-library.md) — Ch. 33 — Batch 7
- [`noopener noreferrer` for Dynamic Links](book4/noopener-noreferrer-links.md) — Ch. 34 — Batch 7
- [Clickjacking Defense with `frame-ancestors`](book4/csp-frame-ancestors-defense.md) — Ch. 34 — Batch 7
- [Fetch Metadata Isolation Policy](book4/fetch-metadata-isolation.md) — Ch. 34 — Batch 7
- [Framebuster Fallback](book4/framebuster-fallback.md) — Ch. 34 — Batch 7
- [Null-Prototype Objects](book4/null-prototype-object.md) — Ch. 34 — Batch 7
- [Prototype Freezing](book4/object-freeze.md) — Ch. 34 — Batch 7
- [Prototype Pollution Key Sanitization](book4/prototype-key-allowlist.md) — Ch. 34 — Batch 7
- [Tabnabbing Defense with COOP](book4/coop-same-origin-defense.md) — Ch. 34 — Batch 7
- [Automated Dependency CVE Scan](book4/automated-cve-dependency-scan.md) — Ch. 35 — Batch 7
- [Exact Dependency Version Pinning](book4/exact-version-pinning.md) — Ch. 35 — Batch 7
- [Full Dependency Tree Inventory](book4/dependency-tree-inventory.md) — Ch. 35 — Batch 7
- [Git SHA Dependency Pinning](book4/git-sha-package-pinning.md) — Ch. 35 — Batch 7
- [Isolate Risky Third-Party Components](book4/isolate-risky-dependency.md) — Ch. 35 — Batch 7
- [JSON Boundary for Third-Party Integration](book4/json-service-boundary.md) — Ch. 35 — Batch 7
- [Multiple Versions of Same Dependency](book4/multi-version-dependency-risk.md) — Ch. 35 — Batch 7
- [npm Shrinkwrap Full Tree Lock](book4/npm-shrinkwrap-tree-lock.md) — Ch. 35 — Batch 7
- [Private Package Mirror](book4/private-package-mirror.md) — Ch. 35 — Batch 7
- [Business-Logic Model Error Analysis](book4/model-error-analysis.md) — Ch. 36 — Batch 7
- [Headless Browser Business-Logic Testing](book4/headless-browser-model-execution.md) — Ch. 36 — Batch 7
- [Statistical Modeling of Inputs](book4/input-statistical-model.md) — Ch. 36 — Batch 7
- [Statistical Modeling of User Actions](book4/action-flow-model.md) — Ch. 36 — Batch 7
- [Worst-Case Scenario Architecture](book4/worst-case-architecture.md) — Ch. 36 — Batch 7

### By Chapter

#### Chapter 2

- [Functional + Technical Recon Model](book4/recon-functional-business-model.md)
- [Hidden Privileged API Inference](book4/hidden-privileged-api-inference.md)
- [JSON-Style Recon Mapping](book4/web-application-map-json.md)
- [RBAC Role Mapping During Recon](book4/rbac-role-mapping.md)
- [Recon Note Relationship Preservation](book4/recon-note-relationship-preservation.md)

#### Chapter 3

- [Arrow Function Context Review](book4/arrow-function-context-review.md)
- [Asynchronous Order Security Review](book4/asynchronous-order-security-review.md)
- [Authentication vs Authorization Map](book4/authentication-vs-authorization-map.md)
- [Browser DOM Security Surface Mapping](book4/dom-security-surface-mapping.md)
- [CDN and Cache Security Mapping](book4/cdn-cache-security-mapping.md)
- [Centralized vs Per-Endpoint Authorization Signal](book4/centralized-authorization-signal.md)
- [Git History Secret Recon](book4/git-history-secret-recon.md)
- [GraphQL Capability Recon](book4/graphql-capability-recon.md)
- [HTTP Basic Authentication Identification](book4/basic-authentication-identification.md)
- [IndexedDB Recon](book4/indexeddb-recon.md)
- [JavaScript `var` Function-Scope Review](book4/var-function-scope-review.md)
- [JavaScript Function Context Analysis](book4/function-context-analysis.md)
- [JavaScript Global Variable Exposure](book4/global-variable-window-exposure.md)
- [JSON Rapid Parsing for Recon](book4/json-rapid-parsing-recon.md)
- [Local Storage Sensitive Data Review](book4/local-storage-sensitive-data-review.md)
- [Modern Multi-Application Architecture Model](book4/modern-multi-application-model.md)
- [Multiple Database Attack Surface](book4/multiple-database-attack-surface.md)
- [OAuth Trust-Boundary Recon](book4/oauth-trust-boundary-recon.md)
- [Prototype Pollution Recon Signal](book4/prototype-pollution-signal.md)
- [REST Resource + HTTP Verb Inference](book4/rest-resource-verb-inference.md)
- [REST Stateless Token Model](book4/rest-stateless-token-model.md)
- [Session Storage Sensitive Data Review](book4/session-storage-sensitive-data-review.md)
- [SPA Framework Detection](book4/spa-framework-detection.md)
- [Swagger/OpenAPI Documentation Discovery](book4/swagger-documentation-discovery.md)
- [Version Control as a Security Boundary](book4/vcs-security-boundary.md)

#### Chapter 4

- [Affiliated Domain Discovery via Browser Network](book4/browser-network-affiliated-domain-discovery.md)
- [Asynchronous DNS Resolution Enumeration](book4/async-dns-resolution-enumeration.md)
- [Dictionary-Based Subdomain Enumeration](book4/dictionary-subdomain-attack.md)
- [DNS Zone Transfer Misconfiguration Test](book4/dns-zone-transfer-test.md)
- [Google `site:` + `-inurl:` Subdomain Discovery](book4/google-site-minus-inurl-subdomains.md)
- [Historical Archive URL Discovery](book4/archive-historical-url-discovery.md)
- [Network Timing Side-Channel Signal](book4/network-timing-side-channel-signal.md)
- [Public Record Secret Discovery](book4/public-record-secret-discovery.md)
- [Social Media Subdomain OSINT](book4/social-media-subdomain-osint.md)
- [Subdomain Brute Force as Last Resort](book4/subdomain-bruteforce-last-resort.md)
- [XHR/Fetch API Endpoint Discovery](book4/xhr-api-endpoint-discovery.md)

#### Chapter 5

- [Application-Specific Payload Shape Inference](book4/application-specific-payload-shape-inference.md)
- [Bearer Token as REST Stateless Signal](book4/rest-bearer-token-stateless-signal.md)
- [HTTP Verb Enumeration](book4/http-verb-enumeration.md)
- [OPTIONS Method Discovery](book4/options-method-discovery.md)
- [Payload Solutions-Space Reduction](book4/solutions-space-reduction.md)
- [REST Endpoint Pattern Recognition](book4/rest-endpoint-pattern-recognition.md)
- [Verbose Error Payload-Shape Disclosure](book4/verbose-error-shape-disclosure.md)

#### Chapter 6

- [Angular Version Detection](book4/angular-version-detection.md)
- [CSS Library Inventory](book4/css-library-inventory.md)
- [Default 404 Fingerprinting](book4/default-404-fingerprinting.md)
- [EmberJS Detection](book4/emberjs-detection.md)
- [External JavaScript Script Inventory](book4/javascript-external-script-inventory.md)
- [MongoDB ObjectId Fingerprinting](book4/mongodb-objectid-fingerprinting.md)
- [Primary-Key Database Detection](book4/primary-key-database-detection.md)
- [Rails 404 Version-Range Fingerprinting](book4/rails-404-version-range-fingerprinting.md)
- [React Version Detection](book4/react-version-detection.md)
- [Server Detection via Response Headers](book4/x-powered-by-server-detection.md)
- [Third-Party Dependency Inventory](book4/third-party-dependency-inventory.md)
- [Vue Version Detection](book4/vue-version-detection.md)

#### Chapter 7

- [Centralized DOM Sanitization Signal](book4/centralized-dom-sanitization-signal.md)
- [Custom Cryptography Risk Signal](book4/custom-crypto-risk-signal.md)
- [Security Layer Count Prioritization](book4/security-layer-count-prioritization.md)
- [Security-by-Design vs Feature-Time Security](book4/security-by-design-vs-feature-time.md)
- [Weakest-Link Layer Analysis](book4/weakest-link-layer-analysis.md)

#### Chapter 8

- [Recon Technique Versioning](book4/recon-technique-versioning.md)

#### Chapter 9

- [Applied Recon to Offense Transition](book4/applied-recon-to-offense.md)

#### Chapter 10

- [`document.write()` XSS Sink](book4/document-write-sink.md)
- [`innerHTML` XSS Sink](book4/innerhtml-sink.md)
- [`window.location.hash` as XSS Source](book4/location-hash-source.md)
- [Browser Tag Auto-Closure Bypass Signal](book4/self-closing-tag-filter-bypass-signal.md)
- [DOM XSS Source/Sink Model](book4/dom-source-sink-model.md)
- [HTML Rendering as an XSS Signal](book4/html-rendering-as-xss-signal.md)
- [Malformed Tag Parser Repair](book4/malformed-tag-parser-repair.md)
- [Mutation-Based XSS Signal](book4/mutation-xss-signal.md)
- [Protocol-Relative URL Filter Bypass Signal](book4/protocol-relative-url-filter-bypass-signal.md)
- [Reflected Query-Parameter XSS](book4/reflected-query-param-xss.md)
- [Reflected XSS Link Delivery](book4/reflected-xss-link-delivery.md)
- [Stored XSS Against Privileged Viewers](book4/stored-xss-privileged-viewer-risk.md)
- [Stored XSS Data Flow](book4/stored-xss-data-flow.md)
- [Unicode Encoding Filter-Bypass Signal](book4/unicode-encoding-filter-bypass-signal.md)
- [XSS Polyglot Context Testing](book4/polyglot-context-testing.md)
- [XSS Sink Inventory](book4/xss-sink-inventory.md)
- [XSS Source Inventory](book4/xss-source-inventory.md)

#### Chapter 11

- [Cross-User CSRF Token Reuse](book4/token-pool-cross-user-reuse.md)
- [CSRF Content-Type Validation Gap](book4/content-type-validation-gap.md)
- [CSRF Regex URL Validator Bypass Signal](book4/regex-url-validator-bypass-signal.md)
- [Iframe GET CSRF](book4/iframe-get-csrf.md)
- [Image-Source GET CSRF](book4/image-src-get-csrf.md)
- [POST Form CSRF](book4/form-post-csrf.md)
- [Predictable CSRF Token Analysis](book4/predictable-token-analysis.md)
- [Referrer/Origin Validation Bypass Signal](book4/referrer-origin-null-bypass-signal.md)
- [State-Changing GET CSRF](book4/get-state-change-csrf.md)
- [Zero-Interaction Form Submission](book4/zero-interaction-form-submit.md)

#### Chapter 12

- [Blind XXE Out-of-Band Detection](book4/oob-callback-detection.md)
- [Direct XXE File-Read Test](book4/direct-external-entity-read.md)
- [Indirect JSON-to-XML XXE Signal](book4/indirect-json-to-xml-conversion.md)
- [XML-Like Input Discovery](book4/xml-like-input-discovery.md)
- [XML-to-Image Parser Chain](book4/xml-to-image-parser-chain.md)
- [XXE Linux Account-File Risk Chain](book4/linux-account-file-risk-chain.md)
- [XXE Password-Hash Escalation Risk](book4/hash-cracking-risk-documentation.md)

#### Chapter 13

- [Authentication Query Injection Risk](book4/sql-auth-query-risk.md)
- [Blind Time-Delay Injection Detection](book4/blind-time-delay-detection.md)
- [CLI Code Injection Signal](book4/cli-code-injection-signal.md)
- [Filename-to-CLI Injection Signal](book4/filename-to-cli-injection.md)
- [In-Band Injection Result Detection](book4/in-band-exfiltration.md)
- [Injection Blocklist Encoding Bypass Signal](book4/blocklist-encoding-bypass-signal.md)
- [OS Command Concatenation Signal](book4/os-command-concatenation-signal.md)
- [Out-of-Band Injection Callback Risk](book4/oob-exfiltration-risk.md)
- [SQL String Concatenation Signal](book4/sql-string-concatenation-signal.md)

#### Chapter 14

- [Autoscaling Cost-Abuse Risk](book4/autoscaling-cost-risk.md)
- [Endpoint Scaling by Account Archetype](book4/scaling-by-account-archetype.md)
- [File Compression DoS Risk](book4/file-compression-dos-risk.md)
- [ReDoS Catastrophic Backtracking](book4/redos-catastrophic-backtracking.md)
- [Resource-Intensive Endpoint Mapping](book4/resource-intensive-endpoint-mapping.md)

#### Chapter 15

- [File IDOR via Direct Filename Reference](book4/file-id-direct-reference.md)
- [Mass Assignment Role Escalation](book4/mass-assignment-role-escalation.md)
- [Mass Assignment via Extra Object Fields](book4/mass-assignment-extra-fields.md)
- [Serializer Identification](book4/serializer-identification.md)
- [Weak Serializer Code-Execution Signal](book4/weak-serializer-code-execution-signal.md)

#### Chapter 16

- [`target=_blank` Tabnabbing Signal](book4/target-blank-tabnabbing-signal.md)
- [Clickjacking Framing Signal](book4/clickjacking-framing-signal.md)
- [Iframe Parent Navigation Risk](book4/iframe-parent-navigation-risk.md)
- [Prototype Pollution Property Injection](book4/prototype-pollution-property-injection.md)
- [Prototype Pollution to Code-Execution Sink](book4/prototype-pollution-to-code-exec-sink.md)
- [Prototype Pollution via Unsafe Merge](book4/prototype-pollution-merge-signal.md)
- [Reverse Tabnabbing via `window.opener`](book4/reverse-tabnabbing-window-opener.md)

#### Chapter 17

- [Branch vs Fork Integration Risk](book4/branch-vs-fork-risk.md)
- [Dependency CVE Cross-Reference](book4/cve-version-cross-reference.md)
- [Direct Source Integration Risk](book4/direct-source-integration-risk.md)
- [Malicious Transitive Package Risk](book4/malicious-transitive-package-risk.md)
- [npm Manifest Detection](book4/npm-manifest-detection.md)
- [OSS Integration Risk Mapping](book4/oss-integration-risk-mapping.md)
- [Package Maintainer Account Compromise Risk](book4/maintainer-account-compromise-risk.md)
- [Self-Hosted Installer Risk](book4/self-hosted-installer-risk.md)
- [Transitive Dependency Risk](book4/package-manager-transitive-risk.md)

#### Chapter 18

- [IEEE754 Financial Precision Risk](book4/ieee754-financial-precision.md)
- [Intended vs Programmed Business Rules](book4/intended-vs-programmed-rules.md)
- [Local vs Global Price Validation](book4/local-vs-global-price-validation.md)
- [Missing Balance Validation](book4/missing-balance-validation.md)
- [Negative Numeric Edge Case](book4/negative-value-edge-case.md)
- [Programmed Side-Effect Abuse](book4/side-effect-abuse.md)
- [Quasi-Cash Reward Loop](book4/quasi-cash-reward-loop.md)
- [Refund + Reward Retention Check](book4/refund-reward-retention.md)
- [Use-Case Edge-Case Modeling](book4/use-case-edge-case-modeling.md)

#### Chapter 19

- [Live Offensive Testing Safety](book4/offense-live-testing-safety.md)

#### Chapter 20

- [Cross-Team Security Review](book4/cross-team-security-review.md)
- [Proactive Vulnerability Discovery Program](book4/proactive-vulnerability-discovery.md)
- [Risk-Based Vulnerability Prioritization](book4/risk-based-vulnerability-prioritization.md)
- [Secure Architecture First](book4/secure-architecture-first.md)
- [Security Code Review Four-Question Baseline](book4/security-code-review-four-questions.md)
- [Temporary Monitoring During Remediation](book4/temporary-monitoring-during-remediation.md)
- [Vulnerability Management Workflow](book4/vulnerability-management-workflow.md)
- [Vulnerability Regression Testing](book4/vulnerability-regression-testing.md)

#### Chapter 21

- [BCrypt Password Storage](book4/bcrypt-password-storage.md)
- [Continuous Authorization After Role Change](book4/continuous-authorization-state-change.md)
- [Data-in-Transit Encryption Requirement](book4/data-in-transit-encryption.md)
- [Feature Requirement Security Review](book4/feature-requirement-security-review.md)
- [MFA Architecture](book4/mfa-architecture.md)
- [Password Entropy Policy](book4/password-entropy-policy.md)
- [Password Hashing Algorithm Selection](book4/password-hashing-choice.md)
- [PBKDF2 Password Storage](book4/pbkdf2-password-storage.md)
- [PII and Financial Data Minimization](book4/pii-financial-data-minimization.md)
- [Search Index Permission Synchronization](book4/search-index-permission-sync.md)
- [Zero Trust Explicit Verification](book4/zero-trust-explicit-verification.md)

#### Chapter 22

- [`X-Content-Type-Options: nosniff`](book4/x-content-type-options-nosniff.md)
- [Cookie Domain Attribute Risk](book4/domain-attribute-risk.md)
- [Cookie Path Minimization](book4/cookie-path-minimization.md)
- [COOP `same-origin`](book4/coop-same-origin.md)
- [CORP Resource Isolation](book4/corp-same-origin.md)
- [CORS Preflight Model](book4/cors-preflight-model.md)
- [CORS Simple Request Model](book4/cors-simple-request-model.md)
- [CORS Wildcard Scope Risk](book4/cors-wildcard-risk.md)
- [CSP `default-src` Baseline](book4/csp-default-src.md)
- [CSP `frame-ancestors` Clickjacking Defense](book4/csp-frame-ancestors.md)
- [CSP `unsafe-inline` / `unsafe-eval` Risk](book4/csp-unsafe-inline-eval-risk.md)
- [CSP Delivery via Header or Meta](book4/csp-header-or-meta.md)
- [CSP Violation Reporting](book4/csp-reporting.md)
- [Hash-Based Strict CSP](book4/strict-csp-hash.md)
- [HSTS Enforcement](book4/hsts-enforcement.md)
- [HttpOnly Cookie Flag](book4/httponly-cookie-flag.md)
- [Iframe Sandbox Attribute](book4/iframe-sandbox-attribute.md)
- [Nonce-Based Strict CSP](book4/strict-csp-nonce.md)
- [Remove `X-Powered-By`](book4/x-powered-by-removal.md)
- [SameSite Strict Cookie](book4/samesite-strict.md)
- [Secure Cookie Flag](book4/secure-cookie-flag.md)
- [Subresource Integrity](book4/subresource-integrity.md)
- [Web Worker Isolation](book4/web-worker-isolation.md)

#### Chapter 23

- [Authentication Enumeration Prevention](book4/authentication-enumeration-prevention.md)
- [Avoid Guessable Identifiers](book4/unguessable-identifiers.md)
- [Enumeration Rate Limits](book4/enumeration-rate-limits.md)
- [Generic User-Facing Error Messages](book4/generic-error-messages.md)
- [Security Light Patterns](book4/security-light-patterns.md)
- [Transaction Outflow Cap](book4/transaction-outflow-cap.md)

#### Chapter 24

- [Attack Vector Cross-Analysis](book4/attack-vector-cross-analysis.md)
- [GraphQL Compute Limits](book4/graphql-compute-limits.md)
- [GraphQL Production Hardening](book4/graphql-production-hardening.md)
- [Internal Actor Worst-Case Modeling](book4/internal-actor-worst-case.md)
- [Privileged Token Scope Reduction](book4/privileged-token-scope.md)
- [Threat Actor Inventory](book4/threat-actor-inventory.md)
- [Threat Model Delta Identification](book4/delta-identification.md)
- [Threat Model Logic Design](book4/logic-design-document.md)
- [Threat Model Mitigation Inventory](book4/mitigation-inventory.md)
- [Threat Model Technical Design](book4/technical-design-document.md)

#### Chapter 25

- [Archetype + Business Logic Review](book4/archetype-plus-business-logic.md)
- [Boilerplate Production Anti-Pattern](book4/boilerplate-production-antipattern.md)
- [Client-to-Server Security Review Path](book4/client-to-server-review-path.md)
- [Client/Server Coupling Anti-Pattern](book4/client-server-coupling-antipattern.md)
- [Local `git diff` Security Review Workflow](book4/local-git-diff-workflow.md)
- [Security Blocklist Anti-Pattern](book4/blocklist-antipattern.md)
- [Security Review at Merge](book4/security-review-at-merge.md)
- [Trust-by-Default Server Account Anti-Pattern](book4/trust-by-default-antipattern.md)

#### Chapter 26

- [Bug Bounty as Discovery Layer](book4/bug-bounty-program-layer.md)
- [CSRF HTTP-Method Regression Test](book4/csrf-method-regression-test.md)
- [Dynamic Analysis Pipeline](book4/dynamic-analysis-pipeline.md)
- [Responsible Disclosure Program](book4/responsible-disclosure-program.md)
- [Security Regression Test Suite](book4/security-regression-tests.md)
- [Static Analysis Pipeline](book4/static-analysis-pipeline.md)
- [Static SQLi/CSRF/DoS Rule Patterns](book4/static-rule-sqli-csrf-dos.md)
- [Static XSS Rule Patterns](book4/static-rule-xss.md)
- [Third-Party Penetration Testing Focus](book4/third-party-pentest-focus.md)

#### Chapter 27

- [Business-Aware Vulnerability Scoring](book4/custom-scoring-extension.md)
- [CVSS Attack Complexity](book4/cvss-attack-complexity.md)
- [CVSS Attack Vector](book4/cvss-attack-vector.md)
- [CVSS Base Scoring](book4/cvss-base-score.md)
- [CVSS Confidentiality/Integrity/Availability Impact](book4/cvss-cia-impact.md)
- [CVSS Environmental Scoring](book4/cvss-environmental.md)
- [CVSS Privileges + User Interaction](book4/cvss-privileges-user-interaction.md)
- [CVSS Temporal Scoring](book4/cvss-temporal.md)
- [Permanent vs Partial Security Fix](book4/permanent-vs-partial-fix.md)
- [Production-Like Vulnerability Reproduction](book4/staging-reproduction.md)
- [Regression Test Required on Closure](book4/regression-on-close.md)
- [Vulnerability Reproduction Logging](book4/reproduction-logging.md)

#### Chapter 28

- [Centralized HTML Sanitization](book4/centralized-html-sanitization.md)
- [CSP Script Source Allowlist](book4/csp-script-src-allowlist.md)
- [Dangerous DOM Sink Reduction](book4/dangerous-dom-sink-removal.md)
- [DOMParser Safe Alternative](book4/domparser-safe-alternative.md)
- [HTML Entity Encoding](book4/html-entity-encoding.md)
- [Hyperlink Canonicalization](book4/hyperlink-canonicalization.md)
- [Prefer Text-Only DOM Insertion](book4/text-only-dom-insertion.md)
- [Remove Eval-Like Code Paths](book4/remove-eval-like-code.md)
- [SVG and Blob Script Risk](book4/svg-blob-risk.md)
- [User-Supplied CSS Risk](book4/user-css-risk.md)

#### Chapter 29

- [Application-Wide Anti-CSRF Middleware](book4/application-wide-middleware.md)
- [No State Changes on GET](book4/no-state-change-on-get.md)
- [Origin + Referer CSRF Check](book4/origin-referer-check.md)
- [Session-Bound CSRF Token](book4/session-bound-csrf-token.md)
- [Stateless CSRF Token](book4/stateless-csrf-token.md)

#### Chapter 30

- [Disable XML External Entities](book4/disable-external-entities.md)
- [Replace XML with Simpler Data Formats](book4/replace-xml-with-json.md)
- [XML Parser Egress Restriction](book4/parser-egress-restriction.md)

#### Chapter 31

- [Database-Specific Escaping as Secondary Defense](book4/database-specific-escaping.md)
- [High-Risk Interpreter Inventory](book4/high-risk-interpreter-inventory.md)
- [Least Authority for Interpreter Modules](book4/least-authority-modules.md)
- [Prepared Statements as Primary SQLi Defense](book4/prepared-statements.md)
- [Server Command Allowlist](book4/command-allowlist.md)
- [SQL Query Inventory](book4/sql-query-inventory.md)

#### Chapter 32

- [DDoS Bandwidth Management](book4/ddos-bandwidth-service.md)
- [DDoS Blackhole Routing](book4/blackhole-routing.md)
- [DoS Resource Risk Tiering](book4/resource-risk-tiering.md)
- [DoS-Oriented Request Performance Logging](book4/request-performance-logging.md)
- [Regex DoS Linting](book4/regex-linting.md)
- [Reject User-Supplied Regex](book4/no-user-supplied-regex.md)

#### Chapter 33

- [Data Transfer Object Defense](book4/data-transfer-object-defense.md)
- [Mass Assignment Field Allowlist](book4/mass-assignment-field-allowlist.md)
- [Object Authorization Before Return](book4/object-authorization-before-return.md)
- [Random Object Reference as Defense-in-Depth](book4/random-object-reference-defense.md)
- [Serialization Type Allowlist](book4/serialization-type-allowlist.md)
- [Strong Serializer Library Selection](book4/strong-serializer-library.md)

#### Chapter 34

- [`noopener noreferrer` for Dynamic Links](book4/noopener-noreferrer-links.md)
- [Clickjacking Defense with `frame-ancestors`](book4/csp-frame-ancestors-defense.md)
- [Fetch Metadata Isolation Policy](book4/fetch-metadata-isolation.md)
- [Framebuster Fallback](book4/framebuster-fallback.md)
- [Null-Prototype Objects](book4/null-prototype-object.md)
- [Prototype Freezing](book4/object-freeze.md)
- [Prototype Pollution Key Sanitization](book4/prototype-key-allowlist.md)
- [Tabnabbing Defense with COOP](book4/coop-same-origin-defense.md)

#### Chapter 35

- [Automated Dependency CVE Scan](book4/automated-cve-dependency-scan.md)
- [Exact Dependency Version Pinning](book4/exact-version-pinning.md)
- [Full Dependency Tree Inventory](book4/dependency-tree-inventory.md)
- [Git SHA Dependency Pinning](book4/git-sha-package-pinning.md)
- [Isolate Risky Third-Party Components](book4/isolate-risky-dependency.md)
- [JSON Boundary for Third-Party Integration](book4/json-service-boundary.md)
- [Multiple Versions of Same Dependency](book4/multi-version-dependency-risk.md)
- [npm Shrinkwrap Full Tree Lock](book4/npm-shrinkwrap-tree-lock.md)
- [Private Package Mirror](book4/private-package-mirror.md)

#### Chapter 36

- [Business-Logic Model Error Analysis](book4/model-error-analysis.md)
- [Headless Browser Business-Logic Testing](book4/headless-browser-model-execution.md)
- [Statistical Modeling of Inputs](book4/input-statistical-model.md)
- [Statistical Modeling of User Actions](book4/action-flow-model.md)
- [Worst-Case Scenario Architecture](book4/worst-case-architecture.md)

## Validation

The consolidated technique files were validated as compact notes (15–40 lines each) rather than reproduced book text.