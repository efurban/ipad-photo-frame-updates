# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-7` (sequence 7), published 2026-10-22: update checks can now show up to three short **What’s new / 更新内容** bullets beneath the version number. Notes follow the selected English/Chinese language and come from the installed updater’s verified local metadata cache. Current-version notes can also be viewed after a successful check. Releases without notes remain compatible.

Install this release once to enable notes for later updates. The existing updater, trust root and five-file app package are unchanged. Local bilingual UI, responsive browser, signed-metadata integration and all 19 updater tests passed; the signed package was verified locally. Installation on the iPad is awaiting verification.

Includes the shuffled-pairing and duplicate-playback fixes from `frame-ota-6`, the Settings redesign and progress feedback from `frame-ota-5`, optional automatic updates from `frame-ota-4`, and gentle photo motion from `frame-ota-3`.
