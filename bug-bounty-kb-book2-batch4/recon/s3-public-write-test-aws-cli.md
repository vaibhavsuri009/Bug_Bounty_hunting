# S3 Public-Write Permission Test

- What it is: A bucket rejects listing/read but still allows unauthenticated or broadly authenticated object writes.
- Use only a harmless uniquely named text file.
- The book's AWS CLI write test:
```bash
aws s3 mv test.txt s3://BUCKET_NAME
```
- If successful, immediately remove your own test object:
```bash
aws s3 rm s3://BUCKET_NAME/test.txt
```
- Confirm target ownership before reporting.
- False positive: write permission to your own authenticated AWS principal may be intentionally delegated.
- Edge case: bucket policies can permit writes but deny deletes, so plan cleanup carefully.
- Remediation: restrict `PutObject/DeleteObject` to explicit trusted principals.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
