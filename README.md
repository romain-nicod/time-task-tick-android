# Time-Task-Tick for Android

Time-Task-Tick is a simple, offline time tracker. You log blocks of time (a date, a start, an end, a description and a category), and the app shows what each day and each week adds up to. It needs no account and no sign-in. It asks for **no permission at all, not even internet access, so it cannot send your data anywhere.** Everything stays on your phone.

This repository holds only the signed installation files (APKs) and the information to check them. There is no source code here.

## Requirements

- Android 8.0 or later.
- An up-to-date **Android System WebView** (updated through the Play Store on most phones). If yours is too old, the app says so and tells you what to update. It never shows a blank screen.

## Install, step by step

1. On your phone, open this repository's **[Releases page](https://github.com/romain-nicod/time-task-tick-android/releases/latest)**. Download only from there, and only from the **latest** release.
2. Download the file named `time-task-tick-X.Y.Z.apk` (X.Y.Z is the version number).
3. Allow your browser to install apps:
   - The simplest way is to open the downloaded file. Android says your phone isn't allowed to install unknown apps from this source. Tap **Settings**, switch on **Allow from this source**, then go back.
   - Or set it in advance. On stock Android 10 to 15: **Settings → Apps → Special app access → Install unknown apps → (your browser) → Allow from this source**. On Android 8 and 9 the first step is **Apps & notifications** instead of **Apps**. If you don't see **Special app access**, look under **Advanced**.
   - Samsung, Xiaomi and other brands use different wording (for example **Special access** behind the ⋮ menu). Search your Settings for "unknown apps".
4. Open the downloaded file and tap **Install**.
5. **Switch "Install unknown apps" off again** for your browser, using the same menu.

**Never turn off Google Play Protect.** The app isn't on the Play Store, so Play Protect may warn you or offer to scan it. Let it scan. If it still warns, first check the file as described below. If the file checks out, tap **More details** and then **Install anyway**. If the check fails, don't install it.

## Verify the file (recommended)

Each release has a `SHA256SUMS` file. Put the APK and `SHA256SUMS` in the same folder on a computer and run one of these:

- Linux: `sha256sum -c SHA256SUMS --ignore-missing`
- macOS: `shasum -a 256 -c SHA256SUMS --ignore-missing`
- Windows (PowerShell): `Get-FileHash .\time-task-tick-X.Y.Z.apk -Algorithm SHA256`, then compare the result with the line in `SHA256SUMS`.

If the values don't match, don't install the file.

**Advanced (signing certificate):** run `apksigner verify --print-certs time-task-tick-X.Y.Z.apk`. The `certificate SHA-256 digest` must be:

```
BE:7C:1A:49:FD:D7:CD:8E:CB:A5:78:9B:AE:AA:56:DB:09:AA:B1:2E:20:61:2A:7D:3C:78:5C:44:F2:75:BC:E7
be7c1a49fdd7cd8ecba5789baeaa56db09aab12e20612a7d3c785c44f275bce7   (same value, as apksigner prints it)
```

## Your data

- Your data stays **on this phone only**. Nothing is copied to the cloud.
- **Uninstalling the app, or clearing its storage, deletes everything.**
- To keep a copy, open the **Backup** tab and tap **Export all**. Android asks you where to save a JSON backup, then a CSV file (for a spreadsheet). Keep them somewhere safe. The Backup tab shows how many days it has been since your last export.
- You can restore a JSON backup from the Backup tab **into an empty app** only.
- A phone-to-phone transfer, when you move to a new phone, may carry your data. Don't count on it: export first.

## Update

Download the newer APK from the Releases page and install it over the app you have. Your data is kept. **Never uninstall to update**, because that deletes your data. Android refuses an older version and refuses a file signed with another certificate. If that happens, stop and report it.

Optional: [Obtainium](https://github.com/ImranR98/Obtainium) can tell you about new releases. Add this repository's address: `https://github.com/romain-nicod/time-task-tick-android`.

## Uninstall

Export your data first (see above). Then press and hold the app icon and choose **Uninstall**, or go to **Settings → Apps → Time-Task-Tick → Uninstall**. This deletes all of its data.

## Privacy

No permission, no account, no analytics, no ads, no network access. The app collects nothing.

## Licence and credits

See [LICENSE](LICENSE) and [NOTICE](NOTICE). The app's **About** screen also lists the third-party licences: the design system (CC BY 4.0), IBM Plex fonts (SIL OFL 1.1) and Bootstrap Icons (MIT).

## Support

Open an issue in this repository's **Issues** tab. Please never attach your backup file: it contains your data.
