# iPad Photo Frame updates

Public distribution of signed application-only updates for the family iPad photo frame.

`metadata/` contains TUF-signed verification metadata. `targets/frame.zip` contains only the app HTML, Python server and layout/shuffle/face helpers. No photos, album links, device settings, credentials or private signing keys are included. The development source repository remains private.

The iPad bootstraps trust from a public root installed over USB and verifies downloads before activation. HTTPS delivery is not a substitute for signature verification.

App adaptation is MIT licensed; the original project is [carlosbaraza/old-ipad-photo-frame](https://github.com/carlosbaraza/old-ipad-photo-frame), commit a7cec3229be1cd644e5f39e92adf6d6b80582edf.

## Current release

`frame-ota-8` (sequence 8), published 2026-10-23: optional **24-hour check / 24 小时检查** in Album & status records playback counts, errors, recoveries and reporting gaps. Diagnostic logs are bounded to 8 MiB and the summary can be copied. The recorder stops after 24 hours and retains its summary; this release does not start it automatically.

Optional private health reports send aggregate summaries every 15 minutes plus a final report to a separately configured Healthchecks log destination. The reporting address is entered once on the iPad, saved privately and omitted from the app package and status/copy responses. Reports are off by default, and a setup test does not start recording. No photos, album links, raw logs or media fingerprints are uploaded. Reporting coverage and review flags are evidence to inspect, not proof that every frame rendered correctly.

Bilingual UI, landscape/portrait/narrow layout, restart persistence, bounded-log/privacy checks, a simulated full day, remote receiver upload/retrieval and all 19 updater tests passed. The signed package was verified against source. Actual 24-hour operation and connectivity from the iPad's network still require device verification.

Includes signed bilingual release notes from `frame-ota-7`, shuffled-pairing and duplicate-playback fixes from `frame-ota-6`, Settings redesign and update progress from `frame-ota-5`, optional automatic updates from `frame-ota-4`, and gentle photo motion from `frame-ota-3`. The existing updater, trust root and five-file app package format are unchanged.
