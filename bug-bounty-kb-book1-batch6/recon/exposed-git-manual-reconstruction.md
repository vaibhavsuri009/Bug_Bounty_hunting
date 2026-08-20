# Manual .git Reconstruction

- **What it is:** Known Git metadata paths are followed from HEAD to refs and objects when directory listing is disabled.
- **Where to look:** A /.git directory where known files are readable but directory contents are not listed.
- **Test / exploitation:**
  - Read .git/HEAD to identify the current branch reference.
  - Fetch the referenced branch file to obtain the commit object hash.
  - Retrieve/decompress the commit object and identify its tree hash.
  - Walk tree objects to discover blob hashes and filenames.
  - Fetch blobs to recover source files, then review them offline.
- **Tools / syntax:**
```text
git cat-file -t OBJECT-HASH
git cat-file -p OBJECT-HASH
```
- **False positives / edge cases:**
  - Remote Git object files are compressed; raw downloaded bytes will not be readable directly.
- **Remediation:** Deny access to all .git paths, not only the directory index.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 21
