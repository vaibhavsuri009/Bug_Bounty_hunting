# HTML Entity Decoding Filter Bypass

- What it is: A filter blocks literal tags but later decodes HTML entities into executable markup.
- Look for fields where `<h1>test</h1>` is neutralized or displayed as plain text.
- Re-submit equivalent markup using numeric HTML entities.
```text
<h1>test</h1>
&#60;&#104;&#49;&#62;test&#60;&#47;&#104;&#49;&#62;
```
- If the encoded form becomes an actual heading, filtering occurred before decoding.
- Expand only enough to prove arbitrary HTML elements can be created.
- Tools: CyberChef is mentioned for testing multiple encoding formats.
- Also test URI-encoded values when the application decodes them before rendering.
- False positive: decoded text is not exploitable if the resulting `<`/`>` are still escaped at the output sink.
- Edge case: different fields may use different decode/filter order.
- Remediation: decode to a canonical form first, then perform output encoding for the final HTML context.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 5
