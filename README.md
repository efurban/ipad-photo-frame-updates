# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-4` (sequence 4), published 2026-10-22: optional automatic installation of verified updates. The English/Chinese switch is off by default and saves immediately. Install this release manually once, then enable **Automatic updates / 自动更新** for later releases. Updates wait for a media boundary or proceed with no recent browser; Settings edits, existing signature checks and rollback are preserved. Local API, browser and existing-supervisor integration checks passed; installation on the iPad is awaiting verification.

Includes the gentle CSS photo motion introduced in `frame-ota-3`.
