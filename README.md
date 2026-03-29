# RepairIQ — Know What You Should Pay

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
