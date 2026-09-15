# Recount

Local voice dictation for Windows. The speech model runs on your own machine — your audio
is never uploaded, stored, or transmitted.

Built for people who document for a living: legal, field inspection, clinical notes.

---

## Status: not yet released

There is no download here yet. This repository exists so the application's update check
has somewhere to look; releases will be published here when the software is ready to sell.

**Before the first release:**

- The installer must be code-signed. An unsigned build triggers a SmartScreen warning,
  which is unacceptable for a product whose premise is handling confidential audio.
- Accuracy needs validating against real recorded speech. Every figure measured so far
  comes from synthesised voices, which are cleaner than a person in a room.
- The remote-desktop insertion path needs testing in a real Citrix and RDP session.

## What it does

- **Runs entirely offline.** The model is embedded in the program. There is no upload path
  in the software, no account, and no server.
- **Works where dictation usually fails.** Three text-insertion methods, because no single
  one reaches everywhere — ordinary typing, clipboard paste for Teams and Java targets,
  and real key presses for Citrix and locked-down remote desktops.
- **Ships domain vocabulary** for legal, field inspection and clinical work, already
  loaded rather than waiting for you to add words one at a time.
- **One-time purchase.** No subscription, no per-seat setup fee, no minute allowance.

## Measured accuracy

**6.5%** word error rate across legal, inspection and clinical phrasing, on synthesised
speech. The test set, the audio generator and the harness will ship with the source so the
figure can be reproduced rather than taken on trust.

Notably, a model 3.3× larger improved this by only 1.3 percentage points while costing
3.8× the latency — and fixed *zero* homophone errors, because *principal* versus
*principle* is resolved by meaning, not by acoustics.

## Privacy

Nothing is collected. Audio is converted to text in memory on your machine and discarded.
Two things leave the computer, neither containing anything you dictated: a weekly licence
check that sends only your key, and a daily check for a newer version. Blocking the
application in your firewall prevents both and does not disable dictation.
