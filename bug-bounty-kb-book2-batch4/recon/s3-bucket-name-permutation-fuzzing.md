# S3 Bucket Name Permutation Fuzzing

- What it is: Predictable organization naming conventions are expanded into candidate S3 bucket names.
- Start from observed bucket names or company naming patterns.
- Generate permutations such as `backup`, `images`, `files`, `media`, `marketing`, and `attachments`.
- Use a bucket discovery tool such as the book's `bucket_finder` to check existence/readability.
- Validate ownership before reporting a discovered bucket.
- Do not assume a bucket named after the company belongs to it.
- False positive: globally unique S3 names can be registered by unrelated users.
- Edge case: existence can sometimes be inferred even when listing is denied.
- Remediation: inventory buckets and use randomized/non-predictable naming only as defense in depth.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
