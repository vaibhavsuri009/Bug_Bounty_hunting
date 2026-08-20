# Decompress Exposed Git Objects

- **What it is:** Downloaded Git object files are zlib-compressed and must be inflated before manual inspection.
- **Where to look:** Object files recovered from an exposed remote .git/objects directory.
- **Test / exploitation:**
  - Download the target Git object by its hash-derived path.
  - Inflate the object with a zlib-capable tool.
  - Inspect the object type/content and follow referenced tree/blob hashes.
  - Repeat until the needed source file is reconstructed.
  - Keep analysis offline after collection to reduce requests.
- **Tools / syntax:**
```text
ruby -rzlib -e 'print Zlib::Inflate.new.inflate(STDIN.read)' < OBJECT_FILE
python -c 'import zlib, sys; print repr(zlib.decompress(sys.stdin.read()))' < OBJECT_FILE
```
- **False positives / edge cases:**
  - The exact Python one-liner may require byte-oriented stdin handling depending on interpreter/version.
- **Remediation:** Prevent public retrieval of Git object storage.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 21
