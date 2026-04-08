# RepairIQ - Car Repair Cost Calculator (B2B Shop Edition)
PWA tells consumers fair repair prices + connects to indie shops. Pipeline: Repair lookup → labor/parts → state R2R laws → nearby shops. Features: Estimate/quote/jobs/settings. Stack: Vanilla JS + Capacitor + Electron APK/PWA.

Repo: https://github.com/808cadger/repairiq. Dev: cadger808 (Pearl City, HI).

## Stack & Design System
- Frontend: Vanilla JS (index.html, api-client.js FIRST, avatar-widget.js for Haiku chat)
- Mobile: Capacitor (android/, capacitor.config.json)
- PWA: manifest.json, sw.js (XSS-hardened, CSP-locked)
- APIs: OpenStreetMap Overpass (shops), Claude Haiku (chat)
- CI: .gitea/workflows
- Design: Claude parchment #f5f4ed, Terracotta #c96442 CTAs, ring shadows

## Key Files & Load Order
1. api-client.js (Claude Haiku + AbortController)
2. avatar-widget.js (floating chat all tabs)
3. index.html (tabs: estimate/quote/jobs/settings)

## Commands
npm install
npx cap sync android
cd android && ./gradlew assembleDebug
npm run electron:dist  # If added

## Code Rules — RepairIQ Pipeline
- **Consumer Pipeline**: Repair select → labor rate (state data) → parts → total range → R2R laws → nearby shops
- **B2B Shop**: Quote generation, jobs tab, settings (shop rates)
- **#ASSUMPTION**: State labor data current; TODO: cache + refresh alerts
- **Security**: AbortController all fetches, CSP headers, no eval()
- **Mobile**: Capacitor camera? for damage photos
- **Haiku Chat**: "Explain [repair] labor rates in [state]" | "Find indie shops near [zip]"
- **Phases**: MVP (consumer) → B2B quotes → Jobs CRM → Multi-shop

## AI Prompts — Repair Critical

## Claude Workflow (Auto-Debug ON)
1. Read CLAUDE.md + api-client.js FIRST
2. Run /doctor; fix lint/security
3. Pipeline: "Estimate → Laws → Shops?"
4. Review: "#ASSUMPTIONs? CSP safe? B2B features?"
5. Output: "Debug complete: [tests passed]" + patches
6. Commit: "feat: [estimate|quote|shops|jobs] [desc]"

## Deploy Checklist

**Commit now** → your 5th elite CLAUDE.md (GlowAI/AutoIQ/CourtAide/FarmSense + RepairIQ). Pattern perfected.
