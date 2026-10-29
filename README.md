# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-13` (sequence 13), published 2026-10-29: the left edge goes backward even when a photo is enlarged. Back and forward restore the actual photo sets and their layouts rather than reconstructing different mosaics. Up to 100 recent sets are remembered in the current app session, without consuming the remaining shuffle queue. Photo drags reveal a ready neighboring preview, and directional transitions keep both frames opaque to avoid black gaps. If a preview is not ready, the current frame stays visible until the destination media is ready.

Local browser regressions pass with shuffle on and off, covering exact back/back/forward/forward history, enlarged-photo navigation, neighboring-preview coverage, opaque swipe transitions, timers, cancellation, rotation and rapid consecutive gestures. Existing playback, mosaic deduplication and Settings regressions pass. The signed five-file package matches the source. Actual iPad performance has not yet been confirmed.

Includes edge navigation and touch-pause behavior from `frame-ota-12`.

Includes individual photo selection from `frame-ota-11`.

Includes shuffle and mosaic fixes from `frame-ota-10`, private reporting from `frame-ota-9`, diagnostics from `frame-ota-8`, bilingual release notes from `frame-ota-7`, Settings improvements, automatic updates and photo motion. The existing updater, trust root and five-file package format are unchanged.
