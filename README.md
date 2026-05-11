# RepairIQ

[![Release](https://img.shields.io/github/v/release/808cadger/repairiq?include_prereleases&label=release)](https://github.com/808cadger/repairiq/releases)
[![Last commit](https://img.shields.io/github/last-commit/808cadger/repairiq)](https://github.com/808cadger/repairiq/commits)
[![License](https://img.shields.io/github/license/808cadger/repairiq)](https://github.com/808cadger/repairiq/blob/HEAD/LICENSE)
![Platforms](https://img.shields.io/badge/platform-Web%2FPWA%2C%20Android-2563eb)

Repair cost calculator for fair-price ranges, right-to-repair context, and shop discovery.

## Project Snapshot

| Area | Details |
|------|---------|
| Primary use case | Repair cost calculator for fair-price ranges, right-to-repair context, and shop discovery. |
| Platforms | Web/PWA, Android |
| Core stack | JavaScript, Capacitor, PWA, OpenStreetMap |
| Review first | `index.html`, `android`, `capacitor.config.json`, `package.json` |

## Download Links

| Platform | Link |
|----------|------|
| iOS / iPhone | [Open the PWA in Safari](https://808cadger.github.io/repairiq/) and choose **Share -> Add to Home Screen** |
| Android | [Download the latest APK from GitHub Releases](https://github.com/808cadger/repairiq/releases/latest) |
| Source | [Download the GitHub source ZIP](https://github.com/808cadger/repairiq/archive/refs/heads/main.zip) |
| Repository | [View on GitHub](https://github.com/808cadger/repairiq) |

## Why This Repo Is Worth Reviewing

- Turns repair uncertainty into concrete price guidance.
- Uses public map/data integrations without account friction.
- PWA plus Android packaging supports quick field use.


<!-- INSTALL-START -->
## Install and run

These instructions install and run `repairiq` from a fresh clone.

### Clone
```bash
git clone https://github.com/808cadger/repairiq.git
cd repairiq
```

### Web app
```bash
npm install
python3 -m http.server 8080
```

### Android build/open
```bash
npm run cap:sync
npm run cap:android
```

### Notes
- Use Node.js 22 or newer for the current package set.
- Android builds require Android Studio, a configured SDK, and Java 21 when Gradle is used.

### AI/API setup
- If the app has AI features, add the required provider key in the app settings or local `.env` file.
- Browser-only apps store user-provided API keys on the local device unless a backend endpoint is configured.

### License
- Apache License 2.0. See [`LICENSE`](./LICENSE).
<!-- INSTALL-END -->


[![Last Commit](https://img.shields.io/gitea/last-commit/cadger808/repairiq?gitea_url=https%3A%2F%2Fcodeberg.org&label=last+commit&color=f59e0b&style=flat-square)](https://codeberg.org/cadger808/repairiq)
[![PWA](https://img.shields.io/badge/platform-PWA-f59e0b?style=flat-square)](https://cadger808.codeberg.page/repairiq)

> Car repair cost calculator with right-to-repair state data. Stop overpaying.

RepairIQ tells you the fair price range for any car repair before you walk into a shop — powered by real labor rate data, your state's right-to-repair laws, and a Find-a-Mechanic tab that locates independent shops near you.

## Features

- Repair cost estimator — parts + labor for 50+ common repairs
- Right-to-repair state law lookup (all 50 states)
- Find a Mechanic — independent shops near you via OpenStreetMap
- Shop comparison with ratings and distance
- XSS-hardened, CSP-locked, AbortController for all network calls

## Stack

`Vanilla JS` · `HTML/CSS` · `OpenStreetMap Overpass API` · `Capacitor` · `PWA`

## Install

[**Live App →**](https://cadger808.codeberg.page/repairiq) · [**Download APK →**](https://codeberg.org/cadger808/repairiq/releases/download/v1.0.0/RepairIQ-v1.0.0.apk) · [Releases](https://codeberg.org/cadger808/repairiq/releases)

## Deploy

```bash
npm install
npx cap sync android
cd android && ./gradlew assembleDebug
```

Built by [cadger808](https://codeberg.org/cadger808) · Pearl City, Hawaii
