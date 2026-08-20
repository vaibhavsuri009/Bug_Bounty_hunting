# Android: ADB Device and File Workflow

- **What it is:** Use Android Debug Bridge (ADB) to communicate with a connected test device.
- **Prerequisite:** Enable Developer Options and USB debugging, connect the device, and approve the host.
- **Check connection:** `adb devices -l`.
- **Install APK:** `adb install PATH_TO_APK`.
- **Pull files:** `adb pull REMOTE_PATH LOCAL_PATH`.
- **Push files:** `adb push LOCAL_PATH REMOTE_PATH`.
- **Remediation:** Disable USB debugging on production/user devices when not required.

```bash
adb devices -l
adb install PATH_TO_APK
adb pull REMOTE_PATH LOCAL_PATH
adb push LOCAL_PATH REMOTE_PATH
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
