# DataGuard — installer mirror

A secondary, independent host for the **DataGuard** client installers, so downloads
are not tied to a single origin. The canonical source is the official DataGuard
Telegram bot (open **https://dataguardvpn.fyi**), which always shows the current
version and its SHA-256. This repository only mirrors those same builds.

## Current build

| Platform | Download | SHA-256 |
|---|---|---|
| Android (arm64) | [DataGuard-arm64.apk](../../releases/download/dist/DataGuard-arm64.apk) | `5a1344b0e38e751437aa2738b051a418652806f7e328e24b42609262ca1f296b` |
| Windows | [DataGuard_Setup.exe](../../releases/download/dist/DataGuard_Setup.exe) | `924849bea9f106928d5a0c9a4881ac010f3aee8b30bd6eb9599290ce93c1381d` |

The `dist` release is updated in place on each new version, so these links stay stable.

## Verify before installing

Always confirm the SHA-256 of the downloaded file matches the value shown in the bot:

```powershell
# Windows (PowerShell)
Get-FileHash .\DataGuard_Setup.exe -Algorithm SHA256
```

```bash
# Linux / macOS
sha256sum DataGuard-arm64.apk
```

If the hash does not match, do not install the file — get it from the bot instead.
