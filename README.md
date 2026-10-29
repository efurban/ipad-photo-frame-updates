# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-12` (sequence 12), published 2026-10-29: tap the outer left/right edges to browse photo sets while taps elsewhere select an individual photo. Swipes follow the finger and animate in the chosen direction once the next media is ready. Deliberate slow drags work; short or cancelled drags settle back. Playback waits during touch so sets are not skipped, and stale gestures cannot affect a replacement slide.

Local browser regression tests cover edge taps, selection, long/short/cancelled swipes, timer holds, stale gestures, rapid consecutive drags, rotation and transition cleanup. The signed five-file package and source hashes were verified. Actual iPad performance remains unverified because the device is unavailable.

Includes individual photo selection from `frame-ota-11`.

Includes shuffle and mosaic fixes from `frame-ota-10`, private reporting from `frame-ota-9`, diagnostics from `frame-ota-8`, bilingual release notes from `frame-ota-7`, Settings improvements, automatic updates and photo motion. The existing updater, trust root and five-file package format are unchanged.
