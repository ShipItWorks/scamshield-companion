# Changelog

Public record of changes to scamshield-companion, written from the product page on shipitworks.com. The source is private. Format: [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Release tags exist on the private repository's default branch.

## 2026-11-10 (release v0.3.0)

- 2026-11-10: Land PR #28 merged into main as abd35d3 (10 lane PRs included); no feature label changed this round. Tagged v0.3.0 at abd35d3.

Score 65 / 100 on our own rubric, scored 2026-11-10. Product page: https://shipitworks.com/apps/#scamshield-companion

## 2026-11-08 (release v0.2.3)

- 2026-11-08: Release v0.2.3. The money playbook in First Aid now asks how you paid (card, bank transfer, payment app, gift card, crypto, cash) and shows only the matching steps; unit tests only, UI not run, step wording not checked against FTC or issuer pages (PR 20).
- 2026-11-08: Two more recorded web-build runs: the built app reloads and opens all four tabs with the network off after one visit, message analysis included (OCR offline not covered; emulated offline, not a device) (PR 12); the Phish or Legit deck was played through by button and swipe, progress kept across a reload (PR 25). Neither log states an exit code, so these rows stay Tested with sample data.
- 2026-11-08: Release v0.2.2. Four proof logs were added on main and the README lines scoped to the web build: the saved redacted PNG (black box changed exactly the dragged area, nothing outside it, no metadata chunks; one box, one image), the A/A+ comfort text (16px to 20px, no sideways scroll at 320px, 48px buttons, kept after reload) and the PausePay answer paths and STOP screen. None of the logs states an exit code, so these rows are Tested with sample data, not Proven (PRs 18, 21, 22).
- 2026-11-08: A test now pins the README counts (16 message rules, 4 PausePay questions); vitest 311 passed in the log (PR 16).
- 2026-11-08: The share_target manifest now declares enctype; the Chrome manifest warning went from 1 to 0 and the GET share text still reaches Inspect in the web build. The Android share sheet was not run (PR 27).
- 2026-11-08: CI now runs on the self-hosted runner; the latest run result is not verified (PR 26).

Score 65 / 100 on our own rubric, scored 2026-11-08. Product page: https://shipitworks.com/apps/#scamshield-companion

## 2026-11-07 (release v0.2.1)

- The PausePay STOP screen now has a step to report fraud at ReportFraud.ftc.gov (with a unit test).
- Privacy and network claims are scoped to what the code shows, and the README lists what the app does not do. Recorded checks: the built Android debug app declares CAMERA and no INTERNET or SMS permission (not a release build, not run on a device), and a scripted walk through all four tabs including text recognition requested nothing from any host except the app's own origin (web build, one headless Chrome run). Release v0.2.1.
- 2026-11-07: The note under the video now says the narration line "nothing leaves the device" is not verified: no network capture of the Android app has run and offline use is untested. The video is not re-recorded yet.

Score 71 / 100 on our own rubric, scored 2026-11-01; no score or proof label changed in this update. Product page: https://shipitworks.com/scamshield-companion/
