# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-19` (sequence 19), published 2026-10-30: completed photo swipes transfer decoded preview images directly into the live slide. The zoom fallback introduced in frame-ota-17 is removed, and neighbor warming again waits until after the slide transition. A synchronous preview transfer does not leave a media-load watchdog armed against an already displayed photo.

Local browser tests exercise repeated left/right reversals with shuffle enabled and disabled, old-Safari image decoding fallback, exact image-element reuse, preserved photo sets and queue state, pinch zoom, cancellation, rotation and video startup. The signed five-file package matches the tested source. Physical-device responsiveness still needs confirmation after installation.

Includes completed video swipes during decoder startup from `frame-ota-18`.

Includes private Axiom health monitoring and prompt album summaries from `frame-ota-16`. Photos, album links, raw filenames and private reporting credentials are excluded from the package. Existing device data and the stable updater remain unchanged.

Includes cached swipes and pinch-to-zoom from `frame-ota-14`.

Includes exact photo-set history and opaque swipe transitions from `frame-ota-13`.

Includes edge navigation and touch-pause behavior from `frame-ota-12`.

Includes individual photo selection from `frame-ota-11`.

Includes shuffle and mosaic fixes from `frame-ota-10`, private reporting from `frame-ota-9`, diagnostics from `frame-ota-8`, bilingual release notes from `frame-ota-7`, Settings improvements, automatic updates and photo motion. The existing updater, trust root and five-file package format are unchanged.
