# Troubleshooting

Having trouble with VARYNX? This guide covers the most common issues and how to resolve them.

---

## General

### The app crashes on launch

1. Force-stop the app: **Settings → Apps → VARYNX → Force Stop**.
2. Clear the app cache: **Settings → Apps → VARYNX → Storage → Clear Cache**.
3. Restart your device and reopen VARYNX.
4. If the crash persists, uninstall and reinstall from Google Play.

If none of the above help, please [open a bug report](https://github.com/M4urk/VARYNX/issues/new?template=bug_report.md) and include any error text you see.

---

### The security score is stuck or not updating

- The score refreshes on a background interval. Pull down on the Dashboard to force a refresh.
- Make sure VARYNX is not battery-optimized: **Settings → Battery → Battery Optimization → VARYNX → Don't Optimize**.
- Check that the relevant features (Bluetooth, Wi-Fi, etc.) are enabled inside VARYNX Settings.

---

### Alerts are not appearing

1. Confirm alerts are enabled in **VARYNX → Settings → Alerts**.
2. Check your device notification settings: **Settings → Apps → VARYNX → Notifications** and make sure notifications are allowed.
3. If you use a custom launcher or notification manager, make sure it is not suppressing VARYNX notifications.
4. Verify that the sensitivity level is not set to **Off**.

---

## Bluetooth Monitoring

### Bluetooth monitoring shows no devices

- Bluetooth must be enabled on your device for VARYNX to scan.
- Grant the **Nearby Devices** (Bluetooth) permission: **Settings → Apps → VARYNX → Permissions → Nearby Devices**.
- On Android 13+, the `BLUETOOTH_SCAN` permission is required. If VARYNX did not ask for this on install, revoke and re-grant the permission.

---

## Wi-Fi Scanning

### Wi-Fi scan results are empty or stale

- Android throttles Wi-Fi scans to protect battery. VARYNX uses the platform scan API and is subject to this limit (typically 4 scans per 2 minutes in the foreground).
- Make sure Wi-Fi is turned on and Location permission is granted (required by Android for Wi-Fi scanning): **Settings → Apps → VARYNX → Permissions → Location**.
- Toggle Wi-Fi off and back on, then return to the VARYNX dashboard.

---

## NFC Detection

### NFC alerts are not triggering

- NFC must be enabled on your device: **Settings → Connected Devices → NFC**.
- VARYNX can only detect NFC interactions while the app is in the foreground or when the screen is on, depending on your Android version.
- Not all devices have NFC hardware. Check your device specifications.

---

## Clipboard Monitoring

### Clipboard monitoring does not work on my device

- On Android 12+, clipboard access from background apps is restricted by the OS. VARYNX uses a foreground approach where possible, but some devices enforce stricter limits.
- This is a platform-level restriction and cannot be bypassed. The feature will still work when VARYNX is in the foreground.

---

## Audit Logs

### Logs are missing or incomplete

- Logs are stored encrypted on-device. If you recently used **Clear All Data**, all logs are permanently deleted.
- Automatic log rotation removes entries older than the configured retention period. Adjust this in **Settings → Log Retention**.
- Export your logs before clearing data: **Settings → Export Data**.

### I cannot open the exported log file

- The export file is a JSON document. Open it with a text editor or any JSON viewer.
- On Android, you can use the **Files** app or share the export to a desktop via USB.

---

## Permissions

### VARYNX keeps asking for a permission I already granted

- Some devices revoke permissions automatically when an app is unused for a few months (Android 11+ auto-reset). Go to **Settings → Apps → VARYNX → Permissions** to re-grant.
- Check for a "Use only while app is in use" restriction on Location or Bluetooth — change it to **Allow all the time** or **While using the app** as prompted.

---

## Data & Privacy

### How do I completely remove all VARYNX data?

Go to **Settings → Clear All Data** inside the app. This permanently deletes all local settings, logs, and alerts. Alternatively, use **Settings → Apps → VARYNX → Storage → Clear Data** on your device.

### Does VARYNX send bug reports automatically?

No. VARYNX makes zero network requests and has no crash reporting SDK. If you experience a bug, please report it manually via [GitHub Issues](https://github.com/M4urk/VARYNX/issues/new?template=bug_report.md).

---

## Still Stuck?

If your issue is not covered here, please [open a bug report](https://github.com/M4urk/VARYNX/issues/new?template=bug_report.md). Include as much detail as possible — especially your Android version, VARYNX version, and the steps that trigger the problem. The more detail you provide, the faster the issue can be fixed.
