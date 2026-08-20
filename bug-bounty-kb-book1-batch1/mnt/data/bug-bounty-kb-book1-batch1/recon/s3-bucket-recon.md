# S3 Bucket Discovery and Access Testing

- What it is: Find organization-linked S3 buckets and safely test whether listing/read/write permissions are exposed.
- Google queries:
```text
site:s3.amazonaws.com COMPANY_NAME
site:amazonaws.com COMPANY_NAME
amazonaws s3 COMPANY_NAME
s3 COMPANY_NAME
```
- Also search public GitHub repositories for `s3` URLs.
- Tools/sources mentioned: GrayhatWarfare, Lazys3, Bucket Stream.
- Install AWS CLI:
```bash
pip install awscli
```
- List bucket contents: `aws s3 ls s3://BUCKET_NAME/`
- Copy a readable test/interesting file: `aws s3 cp s3://BUCKET_NAME/FILE_NAME /local/path/`
- Safe write test: `aws s3 cp TEST_FILE s3://BUCKET_NAME/`
- Remove only your own test object: `aws s3 rm s3://BUCKET_NAME/TEST_FILE`
- Never delete or modify target-owned objects merely to prove impact.
- Remediation: restrict bucket policies/ACLs and prevent unintended public list/read/write access.

## Source: Bug Bounty Bootcamp, Ch. 5
