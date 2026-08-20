# Clickjacking Double-Iframe Frame-Busting Bypass

- **What it is:** Bypasses weak JavaScript frame checks that trust only the top/current frame relationship.
- **Where to look:** Pages blocked by frame-busting JavaScript but lacking robust CSP/X-Frame-Options protections.
- Identify a same-origin target feature that itself allows embedding attacker-controlled or external content in an iframe.
- Place the attacker page inside that trusted target-owned frame, then have the attacker page frame the sensitive target page.
- Weak logic such as `top.location == self.location` may misclassify the nesting as trusted.

```javascript
if (top.location == self.location) {
  // framing allowed
}
```

- **False positives / edge cases:** Modern CSP `frame-ancestors` is enforced by the browser and is not bypassed by this trick.
- **Remediation:** Replace custom frame-busting with CSP `frame-ancestors` and deny unnecessary framing.

## Source: Bug Bounty Bootcamp, Ch. 8
