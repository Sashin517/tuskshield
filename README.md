<div align="center">
  <img src="assets/images/logo_tuskshield.png" alt="TuskShield Logo" height="100">

  # TuskShield (ඇත්පවුර)
  ### Human–Elephant Conflict Alert & Anti-Poaching App
</div>

## Overview

**TuskShield (ඇත්පවුර)** is a community-powered mobile app for reducing human–elephant conflict (HEC) in Sri Lanka. People living and travelling near elephant ranges can report road crossings, injured elephants and poaching activity. Nearby drivers get a full-screen warning when a crossing is verified. Moderators verify reports from a separate admin app.

The project is built in 8 weeks by two developers and runs on a **zero-cost stack**: Flutter, Supabase with PostGIS, OpenStreetMap, and Cloudinary's free tier. Reports also work in rural dead zones: they are saved on the device and sent automatically when signal returns.

This repo holds **two Flutter apps** that share one Supabase backend:

| App | Entrypoint | Audience |
|---|---|---|
| TuskShield User App | `lib/main_user.dart` | Public: villagers, drivers, rangers, volunteers (18 screens) |
| TuskShield Admin App | `lib/main_admin.dart` | Authorized moderators only (6 screens) |

---

## 📋 Task Tracker & Roadmap

**Priority Key:**
🔴 High Priority (Critical) | 🟠 Medium Priority (Enhancement) | 🟡 Low Priority (Polish)

**Status Key:**
✅ Implemented | ⏳ Ongoing | ❌ Not Started

> Statuses below are a starting snapshot. Update them as each sprint closes. The interactive version of this plan, with per-task checklists, lives in the 8-Week Sprint & Team Sync Portal.

**Roles:** **Dev A** = UI and Flutter frontend. **Dev B** = backend, offline engine and admin logic.

### 🎨 Week 1 (Oct 25 – Oct 31): Figma UI Blitz & Backend Foundation
*   🔴 **Master Figma component library and design tokens (Dev A):** ⏳ Ongoing *(Medium Complexity)*
*   🔴 **All 18 User App screens in Figma (Dev A):** ⏳ Ongoing *(High Complexity)*
*   🔴 **All 6 Admin App screens in Figma (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🔴 **Supabase project, PostGIS and Google OAuth (Dev B):** ⏳ Ongoing *(Medium Complexity)*
*   🔴 **SQL migrations for core tables and RLS (Dev B):** ❌ Not Started *(High Complexity)*
*   🟠 **Cloudinary unsigned upload preset and WebP test (Dev B):** ❌ Not Started *(Low Complexity)*
*   🔴 **Kickoff sync: lock DB schema and Figma token contract (Joint):** ❌ Not Started *(Low Complexity)*

### 🌐 Week 2 (Nov 1 – Nov 7): Repository Lock, Models & Onboarding / Auth
*   🔴 **Freeze `pubspec.yaml`, folder boundaries and Dart models (Joint):** ❌ Not Started *(Medium Complexity)*
*   🔴 **Global `AppTheme` and multi-language font switcher (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🔴 **Onboarding screens: Splash, Language, Carousel, Login, Location (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🔴 **Supabase Auth service and Google Sign-In (Dev B):** ❌ Not Started *(Medium Complexity)*
*   🟠 **Mock repositories and geolocation permission handler (Dev B):** ❌ Not Started *(Low Complexity)*

### 🏠 Week 3 (Nov 8 – Nov 14): Home, Quick SOS & Road-Snapping
*   🔴 **5-tab navigation shell and Home Dashboard (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🔴 **Quick SOS bottom sheet with 3 swipe-to-confirm bars (Dev A):** ❌ Not Started *(High Complexity)*
*   🟠 **Swipeable Active Alerts stack and calm-jungle empty state (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🔴 **Import Sri Lanka highway geometry into PostGIS (Dev B):** ❌ Not Started *(Medium Complexity)*
*   🔴 **`ST_DWithin` 50 m road-crossing validation RPC (Dev B):** ❌ Not Started *(High Complexity)*

### 🐘 Week 4 (Nov 15 – Nov 21): Incident Reporting & Photo Pipeline
*   🔴 **Elephants feed and category-first report form (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🔴 **Anti-poaching feed and mandatory-photo anonymous form (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🔴 **On-device WebP compression (~120 KB) and Cloudinary upload (Dev B):** ❌ Not Started *(Medium Complexity)*
*   🟠 **"I See This Too" corroboration RPC and nickname persistence (Dev B):** ❌ Not Started *(Medium Complexity)*

### 📡 Week 5 (Nov 22 – Nov 28): Offline Outbox & Post Details
*   🔴 **Hive offline outbox, connectivity listener and Workmanager sync (Dev B):** ❌ Not Started *(High Complexity)*
*   🔴 **2-hour expiry for queued road-crossing reports (Dev B):** ❌ Not Started *(Medium Complexity)*
*   🟠 **Unified Post Details with proximity banners (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🟠 **Offline Outbox UI, Account settings and My Submissions (Dev A):** ❌ Not Started *(Medium Complexity)*

### 🗺️ Week 6 (Nov 29 – Dec 5): Community, Road Check & Admin Core
*   🟠 **Road Check: A-to-B safe route planner with OSRM overlay (Dev A):** ❌ Not Started *(High Complexity)*
*   🟠 **Community feed and Add Post screen (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🔴 **Admin login and Verification Center (Dev B):** ❌ Not Started *(Medium Complexity)*
*   🔴 **Admin Incident Queue with 1-tap Verify/Resolve (Dev B):** ❌ Not Started *(Medium Complexity)*

### 🚨 Week 7 (Dec 6 – Dec 12): Verification Loop & Driver SOS
*   🔴 **Full-screen background Driver Warning UI, "500m Ahead" (Dev A):** ❌ Not Started *(High Complexity)*
*   🔴 **FCM + full-screen intent notifications (Dev B):** ❌ Not Started *(High Complexity)*
*   🔴 **Admin Verification Detail, Broadcasts and User Trust Manager (Dev B):** ❌ Not Started *(High Complexity)*
*   🟡 **Admin UI polish (Dev A):** ❌ Not Started *(Low Complexity)*
*   🔴 **End-to-end test: Admin approves, driver phone shows SOS (Joint):** ❌ Not Started *(Medium Complexity)*

### 🚀 Week 8 (Dec 13 – Dec 19): Field Testing & Launch
*   🔴 **Rural field simulation: airplane mode, GPS road-snap, battery audit (Joint):** ❌ Not Started *(High Complexity)*
*   🔴 **Production Supabase RLS security audit and GIST indexes (Dev B):** ❌ Not Started *(Medium Complexity)*
*   🟠 **Sinhala and Tamil typography overflow audit (Dev A):** ❌ Not Started *(Medium Complexity)*
*   🟠 **Seed 15 community conservation stories (Dev A):** ❌ Not Started *(Low Complexity)*
*   🔴 **Signed release APK / Play Store AAB for both apps (Joint):** ❌ Not Started *(Medium Complexity)*

---

## Project Architecture

### 1. Flutter App (`/lib`)
- `main_user.dart` - Entrypoint for the public User App.
- `main_admin.dart` - Entrypoint for the Admin Verification App.
- `core/` - Shared foundation: config, themes, routing, localization, utilities. **Locked after Day 2.**
- `models/` - Shared data contracts (`IncidentModel`, `UserProfileModel`, etc.). **Locked after Day 2.**
- `services/` - **Dev B only.** Auth, database, media, geospatial, offline outbox and notifications. Each service has an interface under `services/interfaces/` so Dev A can build against mocks.
- `shared_widgets/` - **Dev A.** Reusable components (jungle button, swipe slider, status chips, map widget).
- `features_user/` - **Dev A only.** All 18 User App screens, grouped by feature.
- `features_admin/` - **Dev B (logic) + Dev A (UI).** The 6 Admin screens.

### 2. Backend (`/supabase`)
- `migrations/` - Ordered SQL: enable PostGIS, schema, RLS policies, road-snap RPC, trust-score trigger.
- `seed.sql` - Test roads and dummy incidents.
- `config.toml` - Local Supabase CLI configuration.

### 3. Assets (`/assets`)
- `fonts/` - DM Sans, Noto Sans Sinhala, Noto Sans Tamil (offline fallbacks).
- `images/` - Logo, onboarding slides, empty-state graphics.
- `icons/` - Custom map markers (crossing, medical, poaching).
- `l10n/` - `app_en.arb`, `app_si.arb`, `app_ta.arb`.

### 4. Agent Config (`/.agents`)
- `AGENT_RULES.md` - Folder ownership and zero-cost rules for Google Antigravity agents.
- `mcp_config.json` - Supabase/Postgres and GitHub MCP server links.

### Full File Structure

```
tuskshield/
├── .agents/                       # Google Antigravity agent configuration
│   ├── AGENT_RULES.md             # Strict folder boundaries & zero-cost rules
│   └── mcp_config.json            # Supabase/Postgres & GitHub MCP links
│
├── supabase/                      # Dev B: backend database & PostGIS SQL
│   ├── config.toml
│   ├── seed.sql
│   └── migrations/
│       ├── 20261025000001_enable_postgis.sql
│       ├── 20261025000002_create_schema.sql
│       ├── 20261025000003_rls_policies.sql
│       ├── 20261025000004_road_snap_rpc.sql
│       └── 20261025000005_trust_score_trig.sql
│
├── assets/
│   ├── fonts/                     # DMSans, NotoSansSinhala, NotoSansTamil
│   ├── images/                    # logo, onboarding_1..3, empty states
│   ├── icons/                     # pin_elephant_crossing, pin_medical_emergency, pin_poaching_alert
│   └── l10n/                      # app_en.arb, app_si.arb, app_ta.arb
│
├── lib/
│   ├── main_user.dart             # Entrypoint 1: public User App
│   ├── main_admin.dart            # Entrypoint 2: Admin Verification App
│   ├── core/                      # Locked after Day 2 (config, theme, routing, localization, utils)
│   ├── models/                    # Locked after Day 2 (shared data contracts)
│   ├── services/                  # Dev B only (auth, database, media, geospatial, offline_outbox, notifications)
│   ├── shared_widgets/            # Dev A: reusable UI components
│   ├── features_user/             # Dev A only: 18 User App screens
│   └── features_admin/            # Dev B (logic) + Dev A (UI): 6 Admin screens
│
├── test/                          # Unit and widget tests
├── .env.example                   # Template for API keys (committed)
├── .gitignore                     # Ignores .env, build/, local Hive boxes
├── analysis_options.yaml          # Strict Flutter lint rules
└── pubspec.yaml                   # Locked dependencies & font/asset declarations
```

> The fully annotated tree, with every file and its purpose, is in the Tutorials and Antigravity tab of the sprint portal.

---

## How to Run Locally

### Prerequisites
- Flutter SDK (stable channel) with an Android emulator or a physical Android device
- [Supabase CLI](https://supabase.com/docs/guides/cli) and Docker (for the local database)
- A free [Supabase](https://supabase.com) project and a free [Cloudinary](https://cloudinary.com) account
- Git

### Step 1: Set Up the Backend
1. Start the local Supabase stack and apply every migration plus the seed data:
   ```bash
   supabase start
   supabase db reset
   ```
2. Confirm PostGIS is enabled and the `roads` table has rows, since the road-snap check depends on it.

### Step 2: Configure the Application
1. Copy the example environment file:
   ```bash
   cp .env.example .env
   ```
2. Fill in your Supabase URL, Supabase anon key and Cloudinary unsigned upload preset. These are read by `lib/core/config/env_config.dart`. Use the variable names listed in `.env.example`.
3. Never commit `.env`. It is already in `.gitignore`.

### Step 3: Install Dependencies
```bash
flutter pub get
flutter gen-l10n
```

### Step 4: Run the App
Run the **User App**:
```bash
flutter run -t lib/main_user.dart
```
Run the **Admin App**:
```bash
flutter run -t lib/main_admin.dart
```

### Step 5: Run Tests
```bash
flutter test
```

---

## Key Features

### User App
- **Language first:** switch between සිංහල, English and தமிழ் on the very first interactive screen.
- **Quick SOS:** three pocket-dial-proof swipe-to-confirm bars (Road Crossing, Medical Elephant, Anti-Poaching) that open the camera and send GPS.
- **Road-snapped reports:** road-crossing pins must be within 50 m of a real road, checked by PostGIS `ST_DWithin`.
- **Road Check:** plan an A-to-B route and see active crossing and medical pins along it.
- **Anonymous anti-poaching reports:** photo required, with Anonymous, saved Nickname or Real Name identity modes. Anonymous reporters are masked at the database level by Row-Level Security.
- **"I See This Too":** one vote per user to corroborate a report.
- **Offline outbox:** reports taken without signal are saved on the device and sent when connectivity returns. Road crossings older than 2 hours expire automatically.
- **Full-screen Driver Warning:** a high-contrast Deep Slate alert ("500 m Ahead") when a crossing is verified nearby, with swipe to dismiss.
- **Community feed:** conservation stories, elephant identification guides and safe-driving tips.

### Admin App
- Secure Official ID and password login.
- Verification Center with quick-stat cards and a live overview map.
- Incident queue with 1-tap Verify, Resolve and Reject/Spam.
- Verification detail view with photo evidence, reporter trust score and a sticky Approve / Resolve / Reject bar.
- Broadcasts to the Community Feed, a top banner or a Driver Alert.
- User Trust management (Trusted, Mute, Ban).

---

## Design System

| Token | Value | Use |
|---|---|---|
| Jungle Green | `#2D6A4F` | Primary actions, brand |
| Safety Amber | `#F59E0B` | Alerts, active crossings |
| Crimson | `#EF4444` | Danger, poaching |
| Soft Gold | `#D97706` | "Buy Us a Coffee" charity button |
| Warm Earth | `#F4F1EA` | App background |
| Deep Slate | `#0F172A` | Driver SOS overlay, Admin login |

**Typography:** DM Sans (English), Noto Sans Sinhala, Noto Sans Tamil.

---

## Tech Stack Reference

- **Frontend:** Flutter (Material 3), GoRouter
- **Backend:** Supabase (PostgreSQL + PostGIS, Auth, Row-Level Security, RPC)
- **Maps and routing:** `flutter_map` with OpenStreetMap, OSRM for routes
- **Media:** `flutter_image_compress` (1080p, 75% WebP, about 120 KB) and Cloudinary unsigned uploads
- **Offline:** Hive, `connectivity_plus`, Workmanager
- **Notifications:** Firebase Cloud Messaging and `flutter_local_notifications` (full-screen intent)
- **Localization:** Flutter `.arb` files for English, Sinhala and Tamil
- **Tooling:** Google Antigravity IDE, Figma

---

## Team Workflow

Two developers with different schedules work in one repo without merge conflicts. This works because each developer owns their own folders.

| Day | Dev A (UI) | Dev B (Backend) | Mode |
|---|---|---|---|
| Mon | Available | 9:30 AM – 2:00 PM | Golden overlap: merge PRs, lock models, pair-debug |
| Tue | Available | 9:30 AM – 2:00 PM | Golden overlap: parallel sprint, live API wiring |
| Wed | Available | 9:30 AM – 2:00 PM | Golden overlap: 1:30 PM pre-handoff sync |
| Thu / Fri | Busy | 9:30 AM – 2:00 PM | Dev B solo backend sprint |
| Sat | Off | Available | Dev B pushes backend PRs to `develop` |
| Sun | Available | Off | Dev A pulls, wires UI, preps Monday sync |

**Rules (also in `.agents/AGENT_RULES.md`):**
- Dev A edits only `lib/features_user/`, `lib/shared_widgets/` and `assets/`.
- Dev B edits only `lib/services/`, `supabase/` and `lib/features_admin/`.
- `pubspec.yaml`, `lib/core/` and `lib/models/` change only after a joint Mon/Tue/Wed 9:30 AM sync.
- Build against the mock services first so UI work is never blocked by the backend.

---

## Deployment

Release builds are produced in Week 8: a signed APK or Play Store AAB for each app (User and Admin), built from the matching entrypoint:

```bash
flutter build appbundle -t lib/main_user.dart
flutter build appbundle -t lib/main_admin.dart
```

Both apps connect to the **same Supabase project**. Admin rights come from an `is_admin` role flag enforced by Row-Level Security, not from a separate backend. Before launch, run the production RLS audit and make sure the PostGIS GIST indexes exist.

---

## Common Issues & Solutions

### Issue: Supabase connection or sign-in fails
**Solution:** Check the URL and anon key in `.env`, and confirm the Google OAuth credentials are set up in both Google Cloud and the Supabase Auth settings. If you use local Supabase, make sure `supabase start` is running.

### Issue: Every road-crossing pin is rejected as "not on a road"
**Solution:** The `roads` table is probably empty. Import only the primary, secondary, tertiary and trunk highways for the HEC zones (Habarana, Anuradhapura, Polonnaruwa, Monaragala, Hambantota) from OpenStreetMap via Overpass. This stays under the free 500 MB database limit.

### Issue: An offline road-crossing report never uploaded
**Solution:** Road-crossing reports older than 2 hours are discarded on purpose, because the crossing is no longer relevant. Medical and anti-poaching reports are kept and uploaded when signal returns.

### Issue: Sinhala or Tamil text shows empty boxes or gets clipped
**Solution:** Make sure the Noto fonts are declared in `pubspec.yaml` and the correct font family is applied for the active locale. Check line height on small screens as part of the Week 8 typography audit.

### Issue: The Driver Warning does not appear when the app is closed
**Solution:** Check that notification and full-screen-intent permissions are granted, and that the FCM payload is sent as high priority. Battery optimization on some phones also blocks background wake-ups.

---

## Notes

- Replace the placeholder names Dev A and Dev B with the team's actual names.
- Check `.env.example` for the exact environment variable names. This README doesn't fix them.
- `.env`, `build/` and local Hive boxes are excluded from Git (see `.gitignore`).
- Seed at least 15 community stories before launch so the Community tab is not empty on day one.