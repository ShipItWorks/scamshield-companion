# ScamShield Companion

Offline-first scam-safety app built around Prevent, Protect, Recover; all analysis on device.

**Score: 71 / 100** on the [ShipItWorks rubric](https://shipitworks.com/how-we-score/). Stage: Beta. As of 2026-11-02, from the [product page](https://shipitworks.com/apps/#scamshield-companion).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Android (PWA wrapped). Not on Google Play yet.

## What works today

- Inspect: Scam Message Coach, LinkLens, PausePay engines
- Harden: Scorecard, Passphrase Coach, Phish or Legit deck
- First Aid MA: playbooks, incident log
- Offline PWA service worker

## Not done yet

- No signed release .aab; the Android build was not run this pass
- No UI tests: the QR scanner, the OCR redact canvas and the Android share intent were never run
- Play listing copy, screenshots and the data-safety form are still missing
- No dark mode; contrast, keyboard and TalkBack never checked
- Offline behaviour itself was never exercised (the service worker builds, but was not run offline)

## Demo

[Transcript of the demo (2:54)](https://shipitworks.com/scamshield-companion/transcript/) · video on the [product page](https://shipitworks.com/apps/#scamshield-companion)

The demo voice is AI-generated (ElevenLabs, "Alice") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README, and soon a CHANGELOG and LICENSE. Until the source is public, the [product page](https://shipitworks.com/apps/#scamshield-companion) is the source of truth, and the score above is the one to trust.

## How we work

Say only what we can back. Say what is not finished before anyone asks. Name people, companies and tools to give credit. Collect as little data as possible. We use AI and say so: Claude (by Anthropic) helps write the code and wrote this README.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02 and reviewed by Robert Sweetman.
