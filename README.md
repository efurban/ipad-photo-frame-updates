# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-18` (sequence 18), published 2026-10-30: returning to a recently played video completes the swipe using its saved frame while the decoder starts. The playing video replaces the frame in place, avoiding a pause halfway across the screen. Playback that starts quickly still permits the swipe animation to finish.

Real-media browser tests cover a 1.6-second startup delay, fast playback, repeated touches, rotation, startup failure, returning from the background and night-mode interruption. Navigation, shuffle, mosaic and pinch regression checks pass. The signed five-file package matches the tested source. Video decoding may still take time on the iPad; this change separates that delay from swipe motion. Physical-device behavior needs confirmation after installation.

Includes earlier preview preparation and first-slide edge handling from `frame-ota-17`.

Includes private Axiom health monitoring and prompt album summaries from `frame-ota-16`. Photos, album links, raw filenames and private reporting credentials are excluded from the package. Existing device data and the stable updater remain unchanged.

Includes cached swipes and pinch-to-zoom from `frame-ota-14`.

Includes exact photo-set history and opaque swipe transitions from `frame-ota-13`.

Includes edge navigation and touch-pause behavior from `frame-ota-12`.

Includes individual photo selection from `frame-ota-11`.

Includes shuffle and mosaic fixes from `frame-ota-10`, private reporting from `frame-ota-9`, diagnostics from `frame-ota-8`, bilingual release notes from `frame-ota-7`, Settings improvements, automatic updates and photo motion. The existing updater, trust root and five-file package format are unchanged.
