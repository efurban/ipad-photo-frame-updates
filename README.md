# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-5` (sequence 5), published 2026-10-22: redesigned English/Chinese Settings with four sections, responsive landscape/portrait cards, and persistent save/back controls. Switching sections preserves unfinished edits. Update checks now show immediate progress, queued status and retry feedback; saving settings also shows a busy label. Local browser, persistence, playback and signed-package checks passed; installation on the iPad is awaiting verification.

Includes optional automatic updates from `frame-ota-4` (off by default; enable in App updates) and gentle CSS photo motion from `frame-ota-3`. Existing settings, signature verification and rollback are preserved.
