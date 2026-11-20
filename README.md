# ScamShield Companion

Offline-first scam-safety app built around Prevent, Protect, Recover; built so analysis runs on the device (offline use not yet tested).

Paused since 18 November 2026, while I finish patchowner. See [patchowner](https://shipitworks.com/patchowner/).

**Score: 65 / 100** on my own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-12; this record was updated 2026-11-18 from the [product page](https://shipitworks.com/scamshield-companion/).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Android (PWA wrapped). Not on Google Play yet.

## What works today

- Inspect: Scam Message Coach, LinkLens, PausePay engines (Tested with sample data)
- Redact: black-box/pixelate (Tested with sample data)
- Harden: Scorecard, Passphrase Coach, Phish or Legit deck (Tested with sample data)
- First Aid MA: playbooks, incident log (Tested with sample data)
- Share-to-app (Android share target / PWA share_target) (Tested with sample data)
- Offline PWA service worker (Tested with sample data)

## Not done yet

- Inspect: camera/photo QR scanner UI (Not tested yet)
- No signed release .aab; a debug APK was built once (permissions dump only) and no release build has run
- The QR scanner ran only in the web build against Chrome's fake capture device and one synthetic QR image (no real camera, no real photos, no Android permission prompt); the Android share sheet was not run; text recognition (OCR) auto-found boxes were not checked; the redacted-PNG check covers one hand-drawn box in the web build; the money playbook is unit-tested only, its UI not run
- Play listing copy, screenshots and the data-safety form are still missing
- No dark mode; contrast, keyboard and TalkBack not checked; comfort text was measured only at an emulated 320px width, not on a phone
- Offline was run once in the web build with Chrome's emulated offline mode (four tabs and one message analysis); offline OCR, airplane mode on a device and the Android app were not run
- No network capture of the Android app on a device: "nothing leaves the device" is not yet traced (web build walk and debug-APK manifest only)
- The PausePay and Phish or Legit advice, card labels and the Massachusetts crypto-kiosk figure on the STOP screen have no expert review or source check on main; money-playbook step wording not checked against FTC or issuer pages
- Privacy policy contact: the placeholder [YOUR CONTACT EMAIL] of ff87049 (2026-11-08) is replaced by support@shipitworks.com in abd35d3 (PRIVACY_POLICY.md:71); whether that mailbox receives mail was not checked
- OCR auto-cover (Auto-Find) did not finish in the Android debug build at 58e4a74 on 2026-11-18: the app asks for eng.traineddata.gz and the build holds eng.traineddata

## What changed

- 2026-11-18: A review of the Android debug build at commit 58e4a74 found that OCR auto-cover (Auto-Find) did not finish, so it was taken out of the Redact line under Works today and added to Not finished. No feature label or score changed.
- 2026-11-12: Merged into the product: a "Load demo data" button in the header that fills the app with invented examples, each marked "Demo data" (a sample message with its verdict, a First Aid recovery record, two log notes and a trusted person called "Sam (demo)"), a card of FBI IC3 cryptocurrency-kiosk figures labelled as a published figure not measured by the app, and a "Clear demo data" button; the header line that made a claim about use without a connection and where data is kept was replaced by a button labelled "Check offline use and privacy yourself" that opens Harden > This app, and the page description was changed to match; and more proof scripts and automated checks. This scorecard round did not run any of it and the recorded runs that the feature labels rest on are older than this code, so no feature label or score changed (PRs #42, #43 and #44). Scorecard rows: no row covers demo data or the header button (not scored); "Inspect: Scam Message Coach, LinkLens, PausePay engines" and "First Aid MA: playbooks, incident log" (both works true, Tested with sample data) are the nearest rows to the screens the demo data fills.
- 2026-11-11: Merged into the app's code: a "Check this app yourself" screen under Harden that shows what Android reports about the installed copy, a First Aid section that lists where the advice comes from and says that no outside expert has reviewed it yet (with a reviewer packet in the repository), a shared email with mail headers that now opens the Email check on Android, a draft privacy-policy section marked not yet published, and more proof scripts and automated checks. This scorecard round did not run any of it and the recorded runs that the feature labels rest on are older than this code, so no feature label or score changed (PRs #35, #34, #38 and #36). Scorecard rows: "Inspect: Scam Message Coach, LinkLens, PausePay engines" and "Share-to-app (Android share target / PWA share_target)" (both works true, Tested with sample data) are the nearest rows to the email check and the shared email; the "Check this app yourself" screen, the advice-sources list with its reviewer packet, and the draft privacy-policy section are not scored (no row covers them).
- 2026-11-11: Merged into the app's code: an email check, a caller check, a trusted-person note, a guided money-recovery flow, an iPhone install card, and opt-in watching of messages and calls on Android, for which the app now asks for the notification permission. The recorded runs that the feature labels rest on are older than this code and this scorecard round did not run it, so no feature label or score changed (PRs #32, #30 and #29).
- 2026-11-10: Land PR #28 merged into main as abd35d3 (10 lane PRs included); no feature label changed this round. Tagged v0.3.0 at abd35d3.
- 2026-11-08: Release v0.2.3. The money playbook in First Aid now asks how you paid (card, bank transfer, payment app, gift card, crypto, cash) and shows only the matching steps; unit tests only, UI not run, step wording not checked against FTC or issuer pages (PR 20).

See [CHANGELOG](CHANGELOG.md).

## Demo

[Transcript of the demo (2:26)](https://shipitworks.com/scamshield-companion/transcript/) · video on the [product page](https://shipitworks.com/scamshield-companion/)

The demo voice is AI-generated (ElevenLabs, "Bella") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README and a CHANGELOG, and soon a LICENSE. Until the source is public, the [product page](https://shipitworks.com/scamshield-companion/) is the source of truth, and the score above is the one to trust.

## How I work

I say only what I can back. I say what is not finished before anyone asks. I name people, companies and tools to give credit. I collect as little data as possible. Built with Claude, by Anthropic: Claude helps write the code and wrote this README. Directed, tested and owned by Robert Sweetman in Stoughton, Massachusetts.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02. Owner review by Robert Sweetman: pending.
