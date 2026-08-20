# Burp Intruder: Fuzzing Workflow

- **What it is:** Use Burp Intruder as an integrated request fuzzer.
- **Start:** Right-click an intercepted request → **Send to Intruder**.
- **Positions:** Highlight the exact request segment to mutate and click **Add**.
- **Payloads:** Select a predefined list or generate values such as numbers/random alphanumeric strings in the Payloads tab.
- **Run:** Start the attack and compare response code, size, content, and timing.
- **Edge case:** Burp Community throttles Intruder; the book suggests Wfuzz/ZAP when speed is needed.
- **Safety:** Throttle fuzzing when necessary to avoid service disruption and follow program rules.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
