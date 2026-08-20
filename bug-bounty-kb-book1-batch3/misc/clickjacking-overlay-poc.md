# Clickjacking Overlay PoC

- **What it is:** Demonstrates whether an invisible framed control can receive a victim's click over a decoy UI.
- **Where to look:** Frameable pages with state-changing actions whose required fields are already populated or controllable.
- Position the target iframe over a benign-looking element.
- Reduce iframe opacity and give it a higher `z-index` so it receives the click.

```css
#victim { position:absolute; opacity:0.00001; z-index:1; }
#decoy  { position:absolute; z-index:-1; }
```

- Align only the minimum test control needed to prove impact on your own account.
- Restore opacity temporarily to verify exact alignment during development.
- **False positives / edge cases:** If the action needs unpredictable typing or extra confirmation, practical exploitability may be low.
- **Remediation:** Prevent untrusted framing and use SameSite cookies for authenticated actions.

## Source: Bug Bounty Bootcamp, Ch. 8
