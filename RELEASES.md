# ANI-KUTA — Releases

How every release on this repository is structured, so users (and future maintainers) can pick the right file and verify it.

## What every release ships

| Asset | What it is |
|---|---|
| `Ani-Kuta-arm64-v8a.apk` | The app for modern 64-bit ARM phones (most devices) |
| `Ani-Kuta-armeabi-v7a.apk` | The app for older 32-bit ARM devices |
| `Ani-Kuta-x86.apk` / `Ani-Kuta-x86_64.apk` | The app for Intel-based devices and emulators |
| `Ani-Kuta-universal.apk` | One APK containing every architecture (largest — pick a specific ABI instead if you can) |
| `Ani-Kuta-<abi>.zip` | The same APK, ZIP-compressed — a smaller download for metered connections; unzip it and install the APK inside |
| `SHA256SUMS.txt` | SHA-256 checksums for every file above |

## Choosing your file

1. **Pick your build**: `arm64-v8a` for modern phones (if unsure, this is almost certainly yours), `armeabi-v7a` for older phones, `x86_64` for PCs/emulators, or `universal` if you want one file that works everywhere.
2. **Pick your format**: the **APK** installs directly; the **ZIP** is the identical APK compressed (typically 30–50% smaller) — unzip it first, then install the APK inside.
3. The download page (https://confused-creature-180.github.io/ANI-KUTA/) picks the right build automatically and lets you switch between APK and ZIP; it shows the real file size of each option.

## Verifying a download

```bash
# compare against SHA256SUMS.txt from the same release:
sha256sum -c SHA256SUMS.txt
```

Every APK inside a ZIP is byte-identical to the standalone APK asset — their SHA-256 hashes match.

## Versioning

- Tags follow `v{major}.{minor}.{patch}` (e.g. `v1.1.3`).
- The in-app updater reads this repository's releases and offers any version newer than the installed one, selecting the APK that matches the device's ABI (universal as the fallback).
- Updates install over an existing installation as long as the version number is higher; no uninstall needed.

## Release checklist (maintainers)

1. Every release carries **both formats** (all APKs + all ZIPs) plus `SHA256SUMS.txt` — never one without the other.
2. Verify every asset's SHA-256 against the checksums file **before** publishing, and again after uploading.
3. Publish releases as **stable + latest**; never re-use or re-point a tag.
4. Release notes: clean, user-facing bullets only (what changed, the ZIP option, the website link, the checksum note) — no commit logs or internal jargon.
5. After publishing: update the download site's version data (both formats + real sizes) and verify the live page, the README links, and an in-app update check from the previous version.
