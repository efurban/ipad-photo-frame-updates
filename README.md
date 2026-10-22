# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-6` (sequence 6), published 2026-10-22: fixes photos on the final screen remaining paired at the end of subsequent shuffled loops. The next loop mixes those photos back into the queue and tries to vary previous companions. Small albums and limited layout choices can still reuse combinations.

Also prevents duplicate references to the same cached photo/video from rewinding navigation into a short repeating section. Existing saved queues and cached manifests normalize those references, and media counts reflect distinct files. Tests cover complete playback loops, restored duplicate queues, album refreshes and sync, settings, server APIs and updater rollback. Two browser scenarios each completed ten loops with every unique photo shown once per loop. The signed package was verified locally; installation on the iPad is awaiting verification.

Includes the bilingual Settings redesign and update progress feedback from `frame-ota-5`, optional automatic updates from `frame-ota-4` (off by default), and gentle CSS photo motion from `frame-ota-3`. Use **Shuffle order / 随机播放 → Yes / 是** for changing combinations.
