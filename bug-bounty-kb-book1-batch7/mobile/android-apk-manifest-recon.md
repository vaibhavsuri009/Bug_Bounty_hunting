# Android: APK and AndroidManifest Recon

- **What it is:** Use APK structure and `AndroidManifest.xml` to map application components, permissions, versions, and libraries.
- **Components:** Activities, Services, BroadcastReceivers, and ContentProviders.
- **Where to look:** Manifest package/version metadata, component declarations, exported interfaces, and permissions.
- **Other useful APK locations:** `classes.dex`, `res/values/strings.xml`, `lib/`, `assets/`, and `META-INF/`.
- **Method:** Start with the manifest to understand attack surface, then pivot into code/resources for specific components.
- **False positives:** Declared components are not automatically exploitable; validate exposure and authorization.
- **Remediation:** Minimize exported components/permissions and enforce authorization at component boundaries.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
