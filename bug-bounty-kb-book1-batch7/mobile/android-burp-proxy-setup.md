# Android: Route App Traffic Through Burp

- **What it is:** Configure Burp to intercept HTTP traffic from an Android test device or emulator.
- **Burp setup:** Proxy → Options → Proxy Listeners → Add; bind an unused port to **All interfaces**.
- **Device setup:** Modify the Wi-Fi network and set proxy host to the computer IP and proxy port to the Burp listener.
- **Linux host IP:** Use `hostname -i`; on macOS the book uses `ipconfig getifaddr en0`.
- **Validation:** Browse from the device and confirm requests appear in Burp.
- **Edge case:** Emulator proxy configuration may live in emulator settings rather than Wi-Fi settings.
- **Safety note:** Do not expose an all-interfaces proxy listener on untrusted/public Wi-Fi.

```bash
hostname -i
ipconfig getifaddr en0
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
