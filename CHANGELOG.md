# Changelog

Public record of changes to scamshield-companion, written from the product page on shipitworks.com. The source is private. Format: [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Release tags exist on the private repository's default branch.

## 2026-11-07 (release v0.2.1)

- The PausePay STOP screen now has a step to report fraud at ReportFraud.ftc.gov (with a unit test).
- Privacy and network claims are scoped to what the code shows, and the README lists what the app does not do. Recorded checks: the built Android debug app declares CAMERA and no INTERNET or SMS permission (not a release build, not run on a device), and a scripted walk through all four tabs including text recognition requested nothing from any host except the app's own origin (web build, one headless Chrome run). Release v0.2.1.
- 2026-11-07: The note under the video now says the narration line "nothing leaves the device" is not verified: no network capture of the Android app has run and offline use is untested. The video is not re-recorded yet.

Score 71 / 100 on our own rubric, scored 2026-11-01; no score or proof label changed in this update. Product page: https://shipitworks.com/scamshield-companion/
