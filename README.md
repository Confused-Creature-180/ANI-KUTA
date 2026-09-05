<div align="center">

# ANI-KUTA

**A clean, extension-based video content application.**

[![Latest Release](https://img.shields.io/github/v/release/Confused-Creature-180/ANI-KUTA?style=flat-square&labelColor=1b1b22)](https://github.com/Confused-Creature-180/ANI-KUTA/releases)
[![Platform](https://img.shields.io/badge/platform-Android-3ddc97?style=flat-square&labelColor=1b1b22)](https://github.com/Confused-Creature-180/ANI-KUTA/releases)
[![Downloads](https://img.shields.io/github/downloads/Confused-Creature-180/ANI-KUTA/total?style=flat-square&labelColor=1b1b22)](https://github.com/Confused-Creature-180/ANI-KUTA/releases)

**[Download](https://confused-creature-180.github.io/ANI-KUTA/)** · **[Releases](https://github.com/Confused-Creature-180/ANI-KUTA/releases)**

</div>

## About

ANI-KUTA is an extension-based video content application with a clean, minimal design. It supports a wide range of extensions, letting you build the content experience you want.

## Download

Head over to the **[download page](https://confused-creature-180.github.io/ANI-KUTA/)** — the site automatically detects your device architecture (`arm64-v8a`, `armeabi-v7a`, or universal) and picks the right build for you.

## Releases

Releases are automated with GitHub Actions:

1. Commit your APKs anywhere in the repository (e.g. `apks/` or `app/build/outputs/apk/**`)
2. Tag and push the version: `git tag v1.0.0 && git push origin v1.0.0`
3. The [release workflow](.github/workflows/release.yml) collects every `*.apk` in the repo and publishes a GitHub Release with auto-generated notes

You can also trigger a release manually from the **Actions** tab (*Release → Run workflow*).

### Recommended APK naming

| File | Architecture |
|---|---|
| `ANI-KUTA-vX.Y.Z-arm64-v8a.apk` | 64-bit ARM (most modern devices) |
| `ANI-KUTA-vX.Y.Z-armeabi-v7a.apk` | 32-bit ARM (older devices) |
| `ANI-KUTA-vX.Y.Z-universal.apk` | All architectures |

## Features

ANI-KUTA is built around the same ideas as the projects that inspired it (Aniyomi, Anikku):

- **Extension-based sources** — bring your own sources through community extensions; the player stays lean
- **Library & categories** — organize your content, schedule refreshes, surface new episodes automatically
- **Local watching** — download and watch offline, anywhere
- **Tracker sync** — keep progress in step with services like AniList, MyAnimeList, Kitsu, Simkl, Shikimori and Bangumi
- **Configurable player** — a video player with the options power users expect
- **Light & dark themes** — follows your device or your mood

> The feature set is in active development — follow along in the repository.

## Build downloads

| Build | Architecture | Devices |
|---|---|---|
| `arm64-v8a` | 64-bit ARM | Most modern Android phones |
| `armeabi-v7a` | 32-bit ARM | Older devices |
| `universal` | All architectures | Safe fallback for anything else |

*Requires Android 8.0 or higher. Not sure which build? The [download page](https://confused-creature-180.github.io/ANI-KUTA/) probes your device and recommends one — entirely in your browser.*

## Disclaimer

The developer(s) of this application have no affiliation with the content providers available through community extensions, and this application hosts zero content. All media is served by third-party sources that the user chooses to install; users are responsible for the content they access and for complying with the laws and terms of service of those providers.

ANI-KUTA is an independent project and is not affiliated with Aniyomi, Anikku, Mihon or Tachiyomi.

## License

To be finalized alongside the first stable release.
