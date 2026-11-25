# VaultTV APK downloads

This public repository contains installation instructions and compiled releases only. Application source, signing material, provider accounts and internal build logs are not distributed here.

**[Download the latest APK](https://github.com/Candyman8019/VaultTV/releases/download/v1.0.0/VaultTV-1.0.0.apk)** · **[Release notes and release date](https://github.com/Candyman8019/VaultTV/releases/latest)** · **[SHA-256 checksum](https://github.com/Candyman8019/VaultTV/releases/download/v1.0.0/VaultTV-1.0.0.apk.sha256)**

The links become available after the first published release. Every release identifies its version and publication date. Previous releases remain available on the Releases page. `version.json` is public metadata needed by the existing in-app updater; it contains no accounts or signing secrets. GitHub-generated source archives for this documentation-only repository contain no application source.

## Amazon Fire TV installation

1. Download the APK through the link above using a compatible download app, or transfer it from a computer.
2. Enable installation for that download/file-manager app under Fire TV Settings → My Fire TV → Developer options → Install unknown apps (wording varies by Fire OS).
3. Open the APK and confirm installation. No GitHub account is needed.
4. Start VaultTV and enter your own authorized M3U or Xtream provider details. No channels, provider credentials or subscriptions are included.

For an existing production installation, install the newer APK over it to retain app data. Updates must use the same package and signing certificate. A previous debug-signed installation cannot be directly updated with the production certificate; arrange a settings backup/migration before any reinstall. Do not uninstall an existing installation casually.

## Other Android devices

Android API 23 (Android 6.0) or newer is the minimum package requirement. The app is designed for TV landscape use with a directional remote. Device/codec/audio compatibility still depends on hardware and source. Allow the browser/file manager to install unknown apps when Android asks, then open and confirm the APK installation.

For authorized ADB installation: `adb install -r VaultTV-1.0.0.apk`. Enable ADB only for your own testing and select the intended device. A newer compatible production APK updates the existing app without clearing data.

## Verify the download

Compare the downloaded APK's SHA-256 with `VaultTV-1.0.0.apk.sha256` from the same release:

```powershell
Get-FileHash .\VaultTV-1.0.0.apk -Algorithm SHA256
```

On Linux/macOS use `sha256sum VaultTV-1.0.0.apk` or `shasum -a 256 VaultTV-1.0.0.apk`. Never install an APK whose checksum does not match.
