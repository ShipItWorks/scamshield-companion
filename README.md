# ScamShield Companion

Offline-first scam-safety app built around Prevent, Protect, Recover; built so analysis runs on the device (offline use not yet tested).

**Score: 65 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-08; this record was updated 2026-11-08 from the [product page](https://shipitworks.com/apps/#scamshield-companion).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Android (PWA wrapped). Not on Google Play yet.

## What works today

- Inspect: Scam Message Coach, LinkLens, PausePay engines (Tested with sample data)
- Redact: black-box/pixelate + OCR auto-cover (Tested with sample data)
- Harden: Scorecard, Passphrase Coach, Phish or Legit deck (Tested with sample data)
- First Aid MA: playbooks, incident log (Tested with sample data)
- Share-to-app (Android share target / PWA share_target) (Tested with sample data)
- Offline PWA service worker (Tested with sample data)

## Not done yet

- Inspect: camera/photo QR scanner UI (Not tested yet)
- No signed release .aab; a debug APK was built once (permissions dump only) and no release build has run
- The QR scanner and the Android share sheet were not run; text recognition (OCR) ran once on one synthetic screenshot and its auto-found boxes were not checked; the redacted-PNG check covers one hand-drawn box in the web build; the money playbook is unit-tested only, its UI not run
- Play listing copy, screenshots and the data-safety form are still missing
- No dark mode; contrast, keyboard and TalkBack not checked; comfort text was measured only at an emulated 320px width, not on a phone
- Offline was run once in the web build with Chrome's emulated offline mode (four tabs and one message analysis); offline OCR, airplane mode on a device and the Android app were not run
- No network capture of the Android app on a device: "nothing leaves the device" is not yet traced (web build walk and debug-APK manifest only)
- The PausePay and Phish or Legit advice, card labels and the Massachusetts crypto-kiosk figure on the STOP screen have no expert review or source check on main; money-playbook step wording not checked against FTC or issuer pages
- Privacy policy contact is still the placeholder [YOUR CONTACT EMAIL] (PRIVACY_POLICY.md:71)

## What changed

- 2026-11-08: Release v0.2.3. The money playbook in First Aid now asks how you paid (card, bank transfer, payment app, gift card, crypto, cash) and shows only the matching steps; unit tests only, UI not run, step wording not checked against FTC or issuer pages (PR 20).
- 2026-11-08: Two more recorded web-build runs: the built app reloads and opens all four tabs with the network off after one visit, message analysis included (OCR offline not covered; emulated offline, not a device) (PR 12); the Phish or Legit deck was played through by button and swipe, progress kept across a reload (PR 25). Neither log states an exit code, so these rows stay Tested with sample data.
- 2026-11-08: Release v0.2.2. Four proof logs were added on main and the README lines scoped to the web build: the saved redacted PNG (black box changed exactly the dragged area, nothing outside it, no metadata chunks; one box, one image), the A/A+ comfort text (16px to 20px, no sideways scroll at 320px, 48px buttons, kept after reload) and the PausePay answer paths and STOP screen. None of the logs states an exit code, so these rows are Tested with sample data, not Proven (PRs 18, 21, 22).
- 2026-11-08: A test now pins the README counts (16 message rules, 4 PausePay questions); vitest 311 passed in the log (PR 16).
- 2026-11-08: The share_target manifest now declares enctype; the Chrome manifest warning went from 1 to 0 and the GET share text still reaches Inspect in the web build. The Android share sheet was not run (PR 27).
- 2026-11-08: CI now runs on the self-hosted runner; the latest run result is not verified (PR 26).

See [CHANGELOG](CHANGELOG.md).

## Demo

[Transcript of the demo (2:54)](https://shipitworks.com/scamshield-companion/transcript/) · video on the [product page](https://shipitworks.com/apps/#scamshield-companion)

The demo voice is AI-generated (ElevenLabs, "Alice") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README and a CHANGELOG, and soon a LICENSE. Until the source is public, the [product page](https://shipitworks.com/apps/#scamshield-companion) is the source of truth, and the score above is the one to trust.

## How we work

Say only what we can back. Say what is not finished before anyone asks. Name people, companies and tools to give credit. Collect as little data as possible. We use AI and say so: Claude (by Anthropic) helps write the code and wrote this README.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02. Owner review by Robert Sweetman: pending.
