# RepairIQ — Know What You Should Pay

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
