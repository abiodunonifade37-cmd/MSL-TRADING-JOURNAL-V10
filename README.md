# MSL Trading Journal V10

A mobile-first, local-first trading journal PWA. No login, Supabase connection, or external database is used.

## Features
- Dashboard, trade log, analytics, playbook, trading models, and a tap-friendly monthly calendar.
- Session reminders for Asia, London, and New York with manually configurable device-local times.
- Browser notifications (permission required), motivational/life reflections, and public-domain Bible verse references. The quote library contains 100 entries.
- Custom journal properties: text, number, or combined text + number; optional dropdown options and required fields.
- Upload trade screenshots directly from the phone. Images are resized and compressed before saving.
- JSON backup and restore; trades, settings, custom fields, models, playbook, and screenshot data are included.
- Offline PWA support, responsive mobile navigation, animated startup screen, dark premium UI.

## Deploy to GitHub Pages
Upload the **contents** of this folder to the root of the existing repository, preserving `assets/`, `index.html`, `styles.css`, `app.js`, `manifest.webmanifest`, and `sw.js`. Commit to the branch configured for GitHub Pages. The same website address can be retained.

## Important data and notification limits
- V10 saves data to browser storage on the current device/browser. It does not sync between devices. Clearing browser data or losing the device can erase journal data; use Download full backup regularly.
- V10 cannot automatically import trades stored only in the old Supabase cloud project. Export those trades before switching if you still need them. The old app's local demo data may be migrated automatically if present in this browser.
- Browser notifications require permission. Session alarms and quote reminders are checked while the app is open or active; a static PWA cannot reliably schedule exact alarms after the browser fully suspends/closes it. For dependable closed-app alarms, a native Android build with native scheduled notifications would be needed.
- The quote library contains 100+ entries, but the app intentionally does not send 100 phone notifications every day. The frequency setting controls occasional reminders while the app is active to avoid notification flooding and OS throttling.
- The app is local-first; screenshot images are compressed, but browser storage is finite. Back up regularly.
