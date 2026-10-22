# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-9` (sequence 9), published 2026-10-23: the family iPad now receives its private health-report destination automatically, with no address to paste. A sealed default is unlocked by the existing private album configuration and saved locally. The package includes no plaintext reporting address, album token or management API key. Saved Off preferences and custom destinations remain unchanged.

After installing, select **Start 24-hour check / 开始 24 小时检查** in Album & status. Applying the default does not start a recording or send a report. Other album configurations can still use manual setup.

Standard Fernet interoperability, default provisioning, wrong-album/tamper rejection, saved preferences, private storage, graceful crypto failure, bilingual Settings and all 19 updater tests passed. The signed five-file app package matches source. Automatic setup and network connectivity on the actual iPad await device verification.

Includes the 24-hour diagnostics, bounded local logs and optional private summary reports introduced in `frame-ota-8`, signed bilingual release notes from `frame-ota-7`, shuffled-playback fixes from `frame-ota-6`, Settings redesign and update progress from `frame-ota-5`, optional automatic updates from `frame-ota-4`, and gentle photo motion from `frame-ota-3`. The existing updater, trust root and five-file package format are unchanged.
