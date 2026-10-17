# Bus Check-In — banner-free wrapper

Two static pages. Each one is nothing but a full-screen frame around the real
Bus Check-In app, which stays hosted on Google exactly where it always was.
This repo doesn't run any code and doesn't touch or store any data — it just
gives people a browser address that doesn't carry Google's own
"created by a Google Apps Script user" banner.

- `index.html` — the kiosk (`?app=kiosk` equivalent), for the iPads
- `hub.html` — the office hub, for signed-in district staff

No student, staff, or district data lives in this repository.

## Home screen (2026-10-03)

`index.html` is home-screen ready: it opens full screen from an iPad home-screen icon, keeps everything dark (no white bounce), and passes its own query through, so `?test=1` opens the kiosk in test mode. The iPad status bar (time, battery) cannot be hidden by any web page. Re-save the home-screen icon from this page after a change to these settings.

## Names (2026-10-14)

Tab title and bookmark name: `index.html` is "APS-T Check-in Kiosk" and `hub.html` is "APS-T Check-in Dashboard". The kiosk's home-screen label (`apple-mobile-web-app-title`) matches; an iPad icon saved earlier keeps its old label until it is removed and re-saved from this page.

## Staging (2026-10-17)

`staging.html` and `staging-hub.html` are the same two wrappers around the staging copy of the app, used for test runs. `staging.html` keeps its device id and offline queue under its own storage keys, because production and staging share this site address and a staging check-in must never reach a production kiosk. Still no code, no data.
