# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-20` (sequence 20), published 2026-10-30: the viewer uses a three-page strip for interruptible swipe motion and quick reversals. It preserves the existing album, shuffle history, media playback, settings, monitoring and signed update flow. A prepared previous photo can be restored while a video is starting.

Targeted browser tests cover photo and video navigation, repeated reversals, interrupted slides, pinch, rotation and shuffle. The signed five-file package matches the tested source. Actual responsiveness on the original iPad still depends on its browser and device conditions.

Includes private Axiom health monitoring and prompt album summaries from `frame-ota-16`. Photos, album links, raw filenames and private reporting credentials are excluded from the package. Existing device data and the stable updater remain unchanged.

Includes cached swipes and pinch-to-zoom from `frame-ota-14`.

Includes exact photo-set history and opaque swipe transitions from `frame-ota-13`.

Includes edge navigation and touch-pause behavior from `frame-ota-12`.

Includes individual photo selection from `frame-ota-11`.

Includes shuffle and mosaic fixes from `frame-ota-10`, private reporting from `frame-ota-9`, diagnostics from `frame-ota-8`, bilingual release notes from `frame-ota-7`, Settings improvements, automatic updates and photo motion. The existing updater, trust root and five-file package format are unchanged.
