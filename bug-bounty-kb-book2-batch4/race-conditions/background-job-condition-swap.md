# Background Job Condition-Swap Race

- What it is: A job captures one condition at queue time but reads changed account data when executing later.
- Look for payments, emails, exports, batch processing, or delayed webhook jobs.
- Trigger the job, then immediately modify the value that controls its destination/recipient.
- Check whether processing uses both the original and updated state.
- The book's HackerOne payment example involved changing a PayPal email during a queued payout workflow.
- Timing may be only seconds, so prepare the change request in advance.
- False positive: duplicate UI receipts do not prove duplicate external processing.
- Edge case: retry queues can complicate timing and evidence.
- Remediation: snapshot immutable job inputs or revalidate atomically at execution time.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 15
