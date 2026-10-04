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
