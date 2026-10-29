# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-14` (sequence 14), published 2026-10-29: prepare and reuse up to two neighboring photo previews (at most six photos in the app's preview cache), decode images ahead of time where supported, prime the page just left for quick reversals, and batch drag updates with requestAnimationFrame. Rotation replaces stale viewport previews. The photo download cache limit is unchanged.

Pinch a photo to view it individually and zoom continuously from 1x to 4x. Drag with one finger to pan within the photo bounds; pinch inward to fit it again. Automatic playback waits until all fingers lift, then resumes with a full interval. Edge taps still navigate; changing sets clears the zoom. Gesture cancellation and rotation cannot accidentally advance the slideshow.

Local browser regressions pass with shuffle on/off and with image.decode unavailable, covering preview reuse without new photo requests, bounded cache size, rotation, pinch/pan limits, finger handoff, cancellation, timer resume and zoom reset. Playback, mosaic comparison, Settings and bilingual release notes tests pass. The signed five-file package matches the source. Actual iPad smoothness has not yet been confirmed.

Includes exact photo-set history and opaque swipe transitions from `frame-ota-13`.

Includes edge navigation and touch-pause behavior from `frame-ota-12`.

Includes individual photo selection from `frame-ota-11`.

Includes shuffle and mosaic fixes from `frame-ota-10`, private reporting from `frame-ota-9`, diagnostics from `frame-ota-8`, bilingual release notes from `frame-ota-7`, Settings improvements, automatic updates and photo motion. The existing updater, trust root and five-file package format are unchanged.
