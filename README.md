# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-10` (sequence 10), published 2026-10-28: shuffle rounds keep their history when a previously shown photo is removed and re-added, and older album responses cannot overwrite newer ones. This prevents two reproducible causes of early repeats during album changes.

When shuffled photos are arranged together, the frame compares tiny in-memory previews of the loaded images. It defers extremely close matches to a later round so they don't appear together. Photos are never deleted. This is a conservative best-effort check: differently cropped matches can be missed, and extremely similar distinct photos may occasionally be deferred. It only compares images within the same set, so visually similar copies appearing separately can still repeat during a round.

Shuffle, actual display-path, album-change, face/layout and browser-canvas tests passed, including differently compressed copies. The signed five-file package was verified against source. The iPad was unavailable for device testing, so actual smoothness and recognition need confirmation there.

Includes the automatic private reporting defaults from `frame-ota-9`, 24-hour diagnostics from `frame-ota-8`, bilingual release notes from `frame-ota-7`, prior shuffled-playback fixes from `frame-ota-6`, Settings improvements from `frame-ota-5`, automatic updates from `frame-ota-4`, and photo motion from `frame-ota-3`. The existing updater, trust root and five-file package format are unchanged.
