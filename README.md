# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-15` (sequence 15), published 2026-10-30: adds private background operational summaries, including playback, album counts, sync, storage and completed loop timing. Reporting only runs when a private, separately provisioned Axiom configuration exists on the device. Photos, album links, raw filenames and credentials are not included in the events or the update package.

The latest slideshow improvements remain included: bounded swipe-preview caching, continuous pinch zoom and panning, photo-set history, bilingual settings and the night clock. Local browser, monitoring, diagnostics and updater tests passed; the signed five-file package matches the source. Device validation follows installation.

Includes cached swipes and pinch-to-zoom from `frame-ota-14`.

Includes exact photo-set history and opaque swipe transitions from `frame-ota-13`.

Includes edge navigation and touch-pause behavior from `frame-ota-12`.

Includes individual photo selection from `frame-ota-11`.

Includes shuffle and mosaic fixes from `frame-ota-10`, private reporting from `frame-ota-9`, diagnostics from `frame-ota-8`, bilingual release notes from `frame-ota-7`, Settings improvements, automatic updates and photo motion. The existing updater, trust root and five-file package format are unchanged.
